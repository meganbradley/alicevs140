---
title: "UUEncode"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 26fc4290-23ed-4f40-935a-93f30edab161
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# UUEncode
Call this function to uuencode some data.  
  
## Syntax  
  
```  
  
      inline BOOL UUEncode(  
   const BYTE* pbSrcData,  
   int nSrcLen,  
   LPSTR szDest,  
   int* pnDestLen,  
   LPCTSTR lpszFile = _T("file"),  
   DWORD dwFlags = 0   
) throw( );  
```  
  
#### Parameters  
 `pbSrcData`  
 The buffer containing the data to be encoded.  
  
 `nSrcLen`  
 The length in bytes of the data to be encoded.  
  
 `szDest`  
 Caller-allocated buffer to receive the encoded data.  
  
 `pnDestLen`  
 Pointer to a variable that contains the length in characters of `szDest`. If the function succeeds, the variable receives the number of characters written to the buffer. If the function fails, the variable receives the required length in characters of the buffer.  
  
 *lpszFile*  
 The file to be added to the header when ATLSMTP_UUENCODE_HEADER is specified in `dwFlags`.  
  
 `dwFlags`  
 Flags controlling the behavior of this function. See [ATLSMTP_UUENCODE Flags](../vs140/ATLSMTP_UUENCODE-Flags.md).  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 This uuencoding implementation follows the POSIX P1003.2b/D11 specification.  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [UUDecode](../vs140/UUDecode.md)   
 [UUDecodeGetRequiredLength](../vs140/UUDecodeGetRequiredLength.md)   
 [UUEncodeGetRequiredLength](../vs140/UUEncodeGetRequiredLength.md)