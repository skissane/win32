---
title: MCIWNDM\_GETEND message
description: The MCIWNDM\_GETEND message retrieves the location of the end of the content of an MCI device or file. You can send this message explicitly or by using the MCIWndGetEnd macro.
ms.assetid: '3fa45928-af63-4f87-835d-f409011a797e'
keywords: ["MCIWNDM_GETEND message Windows Multimedia"]
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
---

# MCIWNDM\_GETEND message

The **MCIWNDM\_GETEND** message retrieves the location of the end of the content of an MCI device or file. You can send this message explicitly or by using the [**MCIWndGetEnd**](mciwndgetend.md) macro.


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## Return Value

Returns the location in the current time format.

## Requirements



|                                     |                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�2000 Professional \[desktop apps only\]<br/>                       |
| Minimum supported server<br/> | Windows�2000 Server \[desktop apps only\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## See also

<dl> <dt>

[**MCIWndGetEnd**](mciwndgetend.md)
</dt> </dl>

�

�




