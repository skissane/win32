---
title: IVMHostInfo OSServicePackString property
description: The OSServicePackString property contains the service pack version currently installed on the host machine.
ms.assetid: 'aae3617e-e7c2-4ea8-a33e-fd8f65f238af'
keywords: ["OSServicePackString property Virtual Server", "OSServicePackString property Virtual Server , IVMHostInfo interface", "IVMHostInfo interface Virtual Server , OSServicePackString property", "OSServicePackString property Virtual Server , VMHostInfo interface", "VMHostInfo interface Virtual Server , OSServicePackString property"]
topic_type:
- apiref
api_name:
- IVMHostInfo.OSServicePackString
- IVMHostInfo.get_OSServicePackString
- VMHostInfo.OSServicePackString
api_location:
- VsComInterfaces.h
api_type:
- COM
---

# IVMHostInfo::OSServicePackString property

The **OSServicePackString** property contains the service pack version currently installed on the host machine.

This property is read-only.

## Syntax


```C++
HRESULT get_OSServicePackString(
  [out]�BSTR *OSServicePack
);
```

<span codelanguage="VisualBasic"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>VMHostInfo.OSServicePackString( _
  ByRef OSServicePack _
)</code></pre></td>
</tr>
</tbody>
</table>



## Property value

The service pack version currently installed on the host machine.

This property value is read-only.

## Error codes



| Name                                                                                          | Meaning                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S\_OK</dt> </dl>              | The operation was successful.<br/>       |
| <dl> <dt>E\_POINTER</dt> </dl>         | The outgoing parameter is **NULL**.<br/> |
| <dl> <dt>DISP\_E\_EXCEPTION</dt> </dl> | An unexpected error occurred.<br/>       |



## Requirements



|                     |                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------|
| Product<br/>  | Microsoft Virtual Server 2005 onWindows Server�2003<br/>                                    |
| Download<br/> | Microsoft Virtual Server 2005 R2 SP1 Update onWindows Server�2008orWindows Server�2003<br/> |
| Header<br/>   | <dl> <dt>VsComInterfaces.h</dt> </dl>      |



## See also

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

�

�




