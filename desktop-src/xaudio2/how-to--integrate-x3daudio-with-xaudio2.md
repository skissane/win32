---
Description: 'This topic shows how to integrate X3DAudio with XAudio2.'
ms.assetid: 'a8f41f0d-b284-aefa-923b-471b13b4a3ec'
title: 'How to: Integrate X3DAudio with XAudio2'
---

# How to: Integrate X3DAudio with XAudio2

This topic shows how to integrate X3DAudio with XAudio2. You can use X3DAudio to provide the volume and pitch values for XAudio2 voices and the parameters for the XAudio2 built in reverb effect. This topic assumes that you have created an audio graph as described in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md). If you have not already created an audio graph, [**X3DAudioInitialize**](x3daudioinitialize.md) will fail.

**To initialize X3DAudio**

1.  Initialize X3DAudio by calling [**X3DAudioInitialize**](x3daudioinitialize.md).

    The [**X3DAudioInitialize**](x3daudioinitialize.md) function takes flags indicating the speaker setup, the speed of sound in user-defined world units per second, and a handle to return an instance of the X3DAudio engine. Call [**IXAudio2MasteringVoice::GetChannelMask**](ixaudio2masteringvoice-interface-getchannelmask.md) to get the output format's channel mask.

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &amp;dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  Create instances of the [**X3DAUDIO\_LISTENER**](x3daudio-listener.md) and [**X3DAUDIO\_EMITTER**](x3daudio-emitter.md) structures.

    The [**X3DAUDIO\_LISTENER**](x3daudio-listener.md) structure represents the position of whatever is hearing the sound. Generally, this is the position of the camera or a position close to it. The [**X3DAUDIO\_EMITTER**](x3daudio-emitter.md) structure represents the position of the thing making the sound. There will be one **X3DAUDIO\_EMITTER** structure for each sound that is being tracked.

    Members of the structures that will not be updated in a game loop should be initialized here. Most members of the structures can simply be initialized to zero. However, some members of [**X3DAUDIO\_EMITTER**](x3daudio-emitter.md) need to be set to be initialized to non-zero values. The ChannelCount member of the **X3DAUDIO\_EMITTER** needs to be initialized to the number of channels in the voice the emitter represents. Also, the CurveDistanceScaler member of **X3DAUDIO\_EMITTER** must be in the range FLT\_MIN to FLT\_MAX.

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  Create an instance of the [**X3DAUDIO\_DSP\_SETTINGS**](x3daudio-dsp-settings.md) structure.

    The [**X3DAUDIO\_DSP\_SETTINGS**](x3daudio-dsp-settings.md) structure is used to return results calculated by [**X3DAudioCalculate**](x3daudiocalculate.md). The **X3DAudioCalculate** function does not allocate memory for any of its parameters. This means that you need to allocate arrays for the **X3DAUDIO\_DSP\_SETTINGS** structure's pMatrixCoefficients and pDelayTimes members if you intend to use them. In addition, you need to set the SrcChannelCount and DstChannelCount members to the number of channels in the emitter's source and destination voices.

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > Use [**IXAudio2Voice::GetVoiceDetails**](ixaudio2voice-interface-getvoicedetails.md) on the mastering voice to obtain the number of InputChannels for **nChannels**. For DirectX SDK versions of XAUDIO2 prior to Windows 8, use IXAudio2::GetDeviceDetails.

     

Perform these steps once every two to three frames to calculate new settings and apply them. In this example, a source voice is sending directly to the mastering voice and to a submix voice with a reverb effect applied to it.

**To use X3DAudio to calculate and apply new 3D audio settings**

1.  Update the [**X3DAUDIO\_LISTENER**](x3daudio-listener.md) and [**X3DAUDIO\_EMITTER**](x3daudio-emitter.md) structures with their current position, velocity, and orientation.

    ```
    Emitter.OrientFront = EmitterOrientFront;
    Emitter.OrientTop = EmitterOrientTop;
    Emitter.Position = EmitterPosition;
    Emitter.Velocity = EmitterVelocity;
    Listener.OrientFront = ListenerOrientFront;
    Listener.OrientTop = ListenerOrientTop;
    Listener.Position = ListenerPosition;
    Listener.Velocity = ListenerVelocity;
    ```

    

2.  Call [**X3DAudioCalculate**](x3daudiocalculate.md) to calculate new settings for the voices.

    The parameters for [**X3DAudioCalculate**](x3daudiocalculate.md) will be the updated [**X3DAUDIO\_LISTENER**](x3daudio-listener.md) and [**X3DAUDIO\_EMITTER**](x3daudio-emitter.md) structures. The flags will indicate what values **X3DAudioCalculate** should calculate, and which [**X3DAUDIO\_DSP\_SETTINGS**](x3daudio-dsp-settings.md) structure will hold the results of the calculations performed.

    ```
    X3DAudioCalculate(X3DInstance, &amp;Listener, &amp;Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &amp;DSPSettings );
    ```

    

3.  Use [**IXAudio2Voice::SetOutputMatrix**](ixaudio2voice-interface-setoutputmatrix.md) and [**IXAudio2SourceVoice::SetFrequencyRatio**](ixaudio2sourcevoice-interface-setfrequencyratio.md) to apply the volume and pitch values to the source voice.

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  Use [**IXAudio2Voice::SetOutputMatrix**](ixaudio2voice-interface-setoutputmatrix.md) to apply the calculated reverb level to the submix voice.

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &amp;DSPSettings.ReverbLevel);
    ```

    

5.  Use [**IXAudio2Voice::SetFilterParameters**](ixaudio2voice-interface-setfilterparameters.md) to apply the calculated low pass filter direct coefficient to the source voice.

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&amp;FilterParameters);
    ```

    

## Related topics

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> <dt>

[X3DAudio Overview](x3daudio-overview.md)
</dt> <dt>

[XAudio2 Programming Guide](programming-guide.md)
</dt> <dt>

[XAudio2 Volume and Pitch Control](volume-and-pitch-control.md)
</dt> </dl>

 

 


