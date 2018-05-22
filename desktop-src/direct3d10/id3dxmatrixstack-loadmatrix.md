﻿---
Description: 'Loads the given matrix into the current matrix.'
ms.assetid: 'b898f344-db90-48e0-b457-0eb8d7b31dca'
title: 'ID3DXMATRIXStack::LoadMatrix method'
---

# ID3DXMATRIXStack::LoadMatrix method

Loads the given matrix into the current matrix.

## Syntax


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## Parameters

<dl> <dt>

*pM* \[in\]
</dt> <dd>

Type: **const [**D3DXMATRIX**](direct3d9.d3dxmatrix)\***

Pointer to the D3DXMATRIX structure loaded into the current matrix.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the method succeeds, the return value is D3D\_OK. If the method fails, the return value can be D3DERR\_INVALIDCALL.

## Remarks

Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.

## Requirements



|                    |                                                                                       |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Library<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## See also

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 



