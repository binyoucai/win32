---
Description: Note  Instead of using this legacy function, we recommend that you use the D3DPreprocess API. Create a shader from a resource without compiling it.
ms.assetid: ca93e208-7627-4bf5-ab83-d4e906e149eb
title: D3DX10PreprocessShaderFromResource function (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type: 
- APIRef
- kbSyntax
api_name: 
- D3DX10PreprocessShaderFromResource
api_type: 
- LibDef
api_location: 
- D3DX10.lib
- D3DX10.dll
---

# D3DX10PreprocessShaderFromResource function

> [!Note]  
> Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.

 

Create a shader from a resource without compiling it.

## Syntax


```C++
HRESULT D3DX10PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## Parameters

<dl> <dt>

*hModule* \[in\]
</dt> <dd>

Type: **[**HMODULE**](../winprog/windows-data-types.md)**

Handle to the resource module containing the shader. HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*pResourceName* \[in\]
</dt> <dd>

Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**

The name of the resource in side hModule containing the shader. If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR. Otherwise, the data type resolves to LPCSTR.

</dd> <dt>

*pSrcFileName* \[in\]
</dt> <dd>

Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**

Optional. Effect file name, which is used for error messages only. Can be **NULL**.

</dd> <dt>

*pDefines* \[in\]
</dt> <dd>

Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***

A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.

</dd> <dt>

*pInclude* \[in\]
</dt> <dd>

Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.

</dd> <dt>

*pPump* \[in\]
</dt> <dd>

Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***

A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)). Use **NULL** to specify that this function should not return until it is completed.

</dd> <dt>

*ppShaderText* \[out\]
</dt> <dd>

Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.

</dd> <dt>

*ppErrorMsgs* \[out\]
</dt> <dd>

Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).

## Requirements



|                    |                                                                                       |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Library<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## See also

<dl> <dt>

[General Purpose Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 