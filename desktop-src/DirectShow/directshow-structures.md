---
Description: DirectShow Structures
ms.assetid: '378f6f43-5c05-4ae4-be24-956f9fc0cacf'
title: DirectShow Structures
---

# DirectShow Structures

This section describes the DirectShow structures.



| Structure                                                                   | Description                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ALLOCATOR\_PROPERTIES**](allocator-properties.md)                       | Contains the allocator's count, size, alignment, and prefix properties.                                                                                                                                               |
| [**AM\_DVD\_RENDERSTATUS**](am-dvd-renderstatus.md)                        | Contains codes indicating the status of DVD-Video playback.                                                                                                                                                           |
| [**AMCOPPCommand**](amcoppcommand.md)                                      | Contains a COPP command.                                                                                                                                                                                              |
| [**AMCOPPSignature**](amcoppsignature.md)                                  | Contains the signature to initiate a Certified Output Protection Protocol (COPP) session.                                                                                                                             |
| [**AMCOPPStatusInput**](amcoppstatusinput.md)                              | Contains a COPP status request.                                                                                                                                                                                       |
| [**AMCOPPStatusOutput**](amcoppstatusoutput.md)                            | Contains the result of a COPP status request.                                                                                                                                                                         |
| [**AM\_MEDIA\_TYPE**](am-media-type.md)                                    | Describes a media type.                                                                                                                                                                                               |
| [**AM\_MPEGSTREAMTYPE**](am-mpegstreamtype.md)                             | Describes an MPEG-1 elementary stream.                                                                                                                                                                                |
| [**AM\_MPEGSYSTEMTYPE**](am-mpegsystemtype.md)                             | Defines the format block for an MPEG-1 system stream.                                                                                                                                                                 |
| [**AM\_SAMPLE2\_PROPERTIES**](am-sample2-properties.md)                    | Describes the properties of a generic media sample.                                                                                                                                                                   |
| [**AM\_STREAM\_INFO**](am-stream-info.md)                                  | Contains start and stop information given to a pin.                                                                                                                                                                   |
| [**AM\_WMT\_EVENT\_DATA**](am-wmt-event-data.md)                           | Contains information pertaining to a WMT\_STATUS event and the associated status code returned by the Windows Media Format SDK.                                                                                       |
| [**AM\_WST\_PAGE**](am-wst-page.md)                                        | Describes a page of WST text.                                                                                                                                                                                         |
| [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md)                           | Contains filter information for registering a filter.                                                                                                                                                                 |
| [**AMOVIESETUP\_MEDIATYPE**](amoviesetup-mediatype.md)                     | Contains media type information for registering a filter.                                                                                                                                                             |
| [**AMOVIESETUP\_PIN**](amoviesetup-pin.md)                                 | Contains pin information for registering a filter.                                                                                                                                                                    |
| [**AMVABeginFrameInfo**](amvabeginframeinfo.md)                            | Specifies information needed to begin processing the frame.                                                                                                                                                           |
| [**AMVABUFFERINFO**](amvabufferinfo.md)                                    | Describes buffer information.                                                                                                                                                                                         |
| [**AMVACompBufferInfo**](amvacompbufferinfo.md)                            | Describes the allocated surfaces and compressed buffer information.                                                                                                                                                   |
| [**AMVAEndFrameInfo**](amvaendframeinfo.md)                                | Specifies information to finish processing the frame.                                                                                                                                                                 |
| [**AMVAInternalMemInfo**](amvainternalmeminfo.md)                          | Specifies the amount of scratch memory the hardware abstraction layer (HAL) will allocate for its private use.                                                                                                        |
| [**AMVAUncompBufferInfo**](amvauncompbufferinfo.md)                        | Describes the surfaces to be allocated.                                                                                                                                                                               |
| [**AMVAUncompDataInfo**](amvauncompdatainfo.md)                            | Specifies the pixel format and dimensional characteristics of the data input stream.                                                                                                                                  |
| [**AMVPDATAINFO**](amvpdatainfo.md)                                        | Specifies the data-specific characteristics of the VP input stream.                                                                                                                                                   |
| [**AMVPDIMINFO**](amvpdiminfo.md)                                          | Specifies the dimensional characteristics of the VP input stream.                                                                                                                                                     |
| [**AMVPSIZE**](amvpsize.md)                                                | Specifies the width and height for a VP image.                                                                                                                                                                        |
| [**ANALOGVIDEOINFO**](analogvideoinfo.md)                                  | Maintains information about the format of the analog video signal.                                                                                                                                                    |
| [**AUDIO\_STREAM\_CONFIG\_CAPS**](audio-stream-config-caps.md)             | Contains information about all possible audio formats supported.                                                                                                                                                      |
| [**AVIMAINHEADER**](avimainheader.md)                                      | Defines global information in an AVI file.                                                                                                                                                                            |
| [**AVIMETAINDEX**](avimetaindex.md)                                        | The base structure for an AVI 2.0 index ('indx' format).                                                                                                                                                              |
| [**AVIOLDINDEX**](avioldindex.md)                                          | Describes an AVI 1.0 index ('idx1' format).                                                                                                                                                                           |
| [**AVIPALCHANGE**](avipalchange.md)                                        | Defines a palette change in an AVI file.                                                                                                                                                                              |
| [**AVISTDINDEX**](avistdindex.md)                                          | Contains an AVI 2.0 standard index.                                                                                                                                                                                   |
| [**AVISTDINDEX\_ENTRY**](avistdindex-entry.md)                             | Contains one index entry for an AVI 2.0 standard index.                                                                                                                                                               |
| [**AVISTREAMHEADER**](avistreamheader.md)                                  | Contains information about one stream in an AVI file.                                                                                                                                                                 |
| [**AVISUPERINDEX**](avisuperindex.md)                                      | Contains an AVI 2.0 super index (index of indexes).                                                                                                                                                                   |
| [**BITMAPINFOHEADER**](bitmapinfoheader.md)                                | Contains information about the dimensions and color format of a device-independent bitmap (DIB).                                                                                                                      |
| [**CodecAPIEventData**](codecapieventdata.md)                              | Describes the event data that an encoder forwards along with an EC\_CODECAPI\_EVENT event.                                                                                                                            |
| [**COLORKEY**](colorkey.md)                                                | Communicates color key information between the renderer and another filter.                                                                                                                                           |
| [**DDCOLORKEY**](ddcolorkey.md)                                            | Describes a color key as a range of values.                                                                                                                                                                           |
| [**DVD\_DECODER\_CAPS**](dvd-decoder-caps.md)                              | Contains information about the audio decoder's capabilities.                                                                                                                                                          |
| [**DVD\_HMSF\_TIMECODE**](dvd-hmsf-timecode.md)                            | Contains timecode information.                                                                                                                                                                                        |
| [**DVD\_MenuAttributes**](dvd-menuattributes.md)                           | Contains information about the menus on a DVD disc.                                                                                                                                                                   |
| [**DVD\_MUA\_Coeff**](dvd-mua-coeff.md)                                    | Contains information about surround sound mixing coefficients for multichannel audio on DVD.                                                                                                                          |
| [**DVD\_MUA\_MixingInfo**](dvd-mua-mixinginfo.md)                          | Contains information about surround sound mixing information on a DVD disc.                                                                                                                                           |
| [**DVD\_MultichannelAudioAttributes**](dvd-multichannelaudioattributes.md) | Contains information about multichannel audio streams on a DVD disc.                                                                                                                                                  |
| [**DVD\_KaraokeAttributes**](dvd-karaokeattributes.md)                     | Contains information about karaoke audio streams on a DVD disc.                                                                                                                                                       |
| [**DVD\_PLAYBACK\_LOCATION**](dvd-playback-location.md)                    | Contains the DVD playback location.                                                                                                                                                                                   |
| [**DVD\_PLAYBACK\_LOCATION2**](dvd-playback-location2.md)                  | Contains the DVD playback location.                                                                                                                                                                                   |
| [**DVD\_SubpictureAttributes**](dvd-subpictureattributes.md)               | Contains information about a subpicture stream on a DVD disc.                                                                                                                                                         |
| [**DVD\_TIMECODE**](dvd-timecode.md)                                       | Contains DVD timecode in hours, minutes, seconds, and frames.                                                                                                                                                         |
| [**DVD\_TitleAttributes**](dvd-titleattributes.md)                         | Contains information about a title on a DVD disc.                                                                                                                                                                     |
| [**DVD\_VideoAttributes**](dvd-videoattributes.md)                         | Contains information about the video stream on a DVD disc.                                                                                                                                                            |
| [**DVINFO**](dvinfo.md)                                                    | Describes the format of a digital video (DV) stream.                                                                                                                                                                  |
| [**FILTER\_INFO**](filter-info.md)                                         | Contains information about a filter.                                                                                                                                                                                  |
| [**HEAACWAVEFORMAT**](heaacwaveformat.md)                                  | Contains format data for an AAC or HE-AAC stream that includes AudioSpecificConfig() data.                                                                                                                            |
| [**HEAACWAVEINFO**](heaacwaveinfo.md)                                      | Contains format data for an Advanced Audio Coding (AAC) or High-Efficiency Advanced Audio Coding (HE-AAC) stream.                                                                                                     |
| [**KSMULTIPLE\_ITEM**](ksmultiple-item.md)                                 | Describes the size and count of variable-length properties on kernel-mode pins.                                                                                                                                       |
| [**KSTOPOLOGY\_CONNECTION**](kstopology-connection.md)                     | Describes a node connection within a kernel streaming (KS) filter.                                                                                                                                                    |
| [**MPEG1VIDEOINFO**](mpeg1videoinfo.md)                                    | Defines the format of MPEG-1 video data.                                                                                                                                                                              |
| [**MPEG1WAVEFORMAT**](mpeg1waveformat.md)                                  | Defines the format of MPEG-1 audio data.                                                                                                                                                                              |
| [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md)                  | Describes the format of MPEG-2 transport stream (TS) packets.                                                                                                                                                         |
| [**MPEG2VIDEOINFO**](mpeg2videoinfo.md)                                    | Contains additional MPEG-2 video system information.                                                                                                                                                                  |
| [**MPEGLAYER3WAVEFORMAT**](mpeglayer3waveformat.md)                        | Describes an MPEG Audio Layer-3 (MP3) audio format.                                                                                                                                                                   |
| [**NORMALIZEDRECT**](normalizedrect.md)                                    | Specifies the location of a video rectangle in composition space.                                                                                                                                                     |
| [**PERFINFO\_DSHOW\_AUDIOBREAK**](perfinfo-dshow-audiobreak.md)            | Data for a trace event of type GUID\_AUDIOBREAK.                                                                                                                                                                      |
| [**PERFINFO\_DSHOW\_AVREND**](perfinfo-dshow-avrend.md)                    | Data for a trace event of type GUID\_VIDEOREND.                                                                                                                                                                       |
| [**PERFINFO\_DSHOW\_STREAMTRACE**](perfinfo-dshow-streamtrace.md)          | Data for a trace event of type GUID\_STREAMTRACE.                                                                                                                                                                     |
| [**PID\_MAP**](pid-map.md)                                                 | Identifies the contents of an MPEG-2 transport stream packet ID.                                                                                                                                                      |
| [**PIN\_INFO**](pin-info.md)                                               | Contains information about a pin.                                                                                                                                                                                     |
| [**Quality**](quality.md)                                                  | Defines a quality-control message.                                                                                                                                                                                    |
| [**REGFILTER2**](regfilter2.md)                                            | Describes a filter for registration through the [**IFilterMapper2**](ifiltermapper2.md) interface.                                                                                                                   |
| [**REGFILTERPINS**](regfilterpins.md)                                      | Contains pin information for registering a filter.                                                                                                                                                                    |
| [**REGFILTERPINS2**](regfilterpins2.md)                                    | Contains information for registering a filter through the [**IFilterMapper2**](ifiltermapper2.md) interface.                                                                                                         |
| [**REGPINMEDIUM**](regpinmedium.md)                                        | Describes a pin medium for registration through the [**IFilterMapper2**](ifiltermapper2.md) interface.                                                                                                               |
| [**REGPINTYPES**](regpintypes.md)                                          | Contains media type information for registering a filter.                                                                                                                                                             |
| [**STREAM\_ID\_MAP**](stream-id-map.md)                                    | Contains information about an elementary stream within an MPEG-2 program stream.                                                                                                                                      |
| [**TIMECODE**](timecode.md)                                                | Contains basic timecode frame count information.                                                                                                                                                                      |
| [**TIMECODE\_SAMPLE**](timecode-sample.md)                                 | Contains complete timecode information.                                                                                                                                                                               |
| [**TRUECOLORINFO**](truecolorinfostructure.md)                             | Maintains color information.                                                                                                                                                                                          |
| [**VIDEO\_STREAM\_CONFIG\_CAPS**](video-stream-config-caps.md)             | Contains information about possible connections.                                                                                                                                                                      |
| [**VIDEOINFO**](videoinfo.md)                                              | Contains information that specifies a video image and its color palette and bitmasks.                                                                                                                                 |
| [**VIDEOINFOHEADER**](videoinfoheader.md)                                  | Describes the bitmap and color information for a video image.                                                                                                                                                         |
| [**VIDEOINFOHEADER2**](videoinfoheader2.md)                                | Describes the bitmap and color information for a video image, including interlace, copy protection, and pixel aspect ratio information.                                                                               |
| [**VMR9AllocationInfo**](vmr9allocationinfo.md)                            | Used to allocate a new bitmap surface by the [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](ivmrsurfaceallocatornotify9-allocatesurfacehelper.md) method. (VMR-9.)                                         |
| [**VMR9AlphaBitmap**](vmr9alphabitmap.md)                                  | Provides a static alpha-blended bitmap to be displayed on the composited video frame supplied by the [**IVMRMixerBitmap9::GetAlphaBitmapParameters**](ivmrmixerbitmap9-getalphabitmapparameters.md) method. (VMR-9.) |
| [**VMR9DeinterlaceCaps**](vmr9deinterlacecaps.md)                          | Describes the capabilities of a deinterlacing mode. (VMR-9.)                                                                                                                                                          |
| [**VMR9Frequency**](vmr9frequency.md)                                      | Describes the frequency of a video stream. (VMR-9.)                                                                                                                                                                   |
| [**VMR9MonitorInfo**](vmr9monitorinfo.md)                                  | Used to set and retrieve information about monitors on the system. (VMR-9.)                                                                                                                                           |
| [**VMR9NormalizedRect**](vmr9normalizedrect.md)                            | Used to specify or retrieve the location of a video rectangle in composition space. (VMR-9.)                                                                                                                          |
| [**VMR9PresentationInfo**](vmr9presentationinfo.md)                        | Used to present video frame information. (VMR-9.)                                                                                                                                                                     |
| [**VMR9ProcAmpControl**](vmr9procampcontrol.md)                            | Specifies the image adjustments to be performed on a video stream. (VMR-9.)                                                                                                                                           |
| [**VMR9ProcAmpControlRange**](vmr9procampcontrolrange.md)                  | Specifies the valid range for an image adjustment property. (VMR-9.)                                                                                                                                                  |
| [**VMR9VideoDesc**](vmr9videodesc.md)                                      | Sescribes a video stream to be deinterlaced. (VMR-9.)                                                                                                                                                                 |
| [**VMR9VideoStreamInfo**](vmr9videostreaminfo.md)                          | Contains video stream information that is used by the VMR-9.                                                                                                                                                          |
| [**VMRALLOCATIONINFO**](vmrallocationinfo.md)                              | Used to allocate a new bitmap surface by the [**IVMRSurfaceAllocator::AllocateSurface**](ivmrsurfaceallocator-allocatesurface.md) method. (VMR-7.)                                                                   |
| [**VMRALPHABITMAP**](vmralphabitmap.md)                                    | Provides a static alpha-blended bitmap to be displayed on the composited video frame supplied by the [**IVMRMixerBitmap::GetAlphaBitmapParameters**](ivmrmixerbitmap-getalphabitmapparameters.md) method. (VMR-7.)   |
| [**VMRGUID**](vmrguid.md)                                                  | Used to identify a monitor on the system. (VMR-7.)                                                                                                                                                                    |
| [**VMRMONITORINFO**](vmrmonitorinfo.md)                                    | Used to set and retrieve information about monitors on the system. (VMR-7.)                                                                                                                                           |
| [**VMRPRESENTATIONINFO**](vmrpresentationinfo.md)                          | Used to present video frame information. (VMR-7.)                                                                                                                                                                     |
| [**VMRVIDEOSTREAMINFO**](vmrvideostreaminfo.md)                            | Contains video stream information that is used in the Video Mixing Renderer filter call to the [**IVMRImageCompositor::CompositeImage**](ivmrimagecompositor-compositeimage.md) method. (VMR-7.)                     |
| [**WAVEFORMATEX**](waveformatex.md)                                        | Defines the format of waveform-audio data.                                                                                                                                                                            |
| [**WAVEFORMATEXTENSIBLE**](waveformatextensible.md)                        | Defines the format of waveform-audio data for formats having more than two channels.                                                                                                                                  |



 

## Related topics

<dl> <dt>

[DirectShow Reference](directshow-reference.md)
</dt> </dl>

 

 


