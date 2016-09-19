---
title: "QPDecode"
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
ms.assetid: c5caf731-9bc4-4740-8899-720f84ed014c
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# QPDecode
Decodes a string of data that has been encoded in quoted-printable format such as by a previous call to [QPEncode](../vs140/QPEncode.md).  
  
## Syntax  
  
```  
inline BOOL QPDecode(  
   BYTE* pbSrcData,  
   int nSrcLen,  
   LPSTR szDest,  
   int* pnDestLen,  
   DWORD dwFlags = 0   
) throw( );  
```  
  
#### Parameters  
 [in] `pbSrcData`  
 The buffer containing the data to be decoded.  
  
 [in] `nSrcLen`  
 The length in bytes of `pbSrcData`.  
  
 [out] `szDest`  
 Caller-allocated buffer to receive the decoded data.  
  
 [out] `pnDestLen`  
 Pointer to a variable that contains the length in bytes of `szDest`. If the function succeeds, the variable receives the number of bytes written to the buffer. If the function fails, the variable receives the required length in bytes of the buffer.  
  
 [in] `dwFlags`  
 Flags describing how the conversion is to be performed. See [ATLSMTP_QPENCODE Flags](../vs140/ATLSMTP_QPENCODE-Flags.md).  
  
## Return Value  
 Returns `TRUE` on success, `FALSE` on failure.  
  
## Remarks  
 The quoted-printable encoding scheme is described in RFC 2045 ([http://www.ietf.org/rfc/rfc2045.txt](http://www.ietf.org/rfc/rfc2045.txt)).  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [QPDecodeGetRequiredLength](../vs140/QPDecodeGetRequiredLength.md)   
 [QPEncode](../vs140/QPEncode.md)   
 [QPEncodeGetRequiredLength](../vs140/QPEncodeGetRequiredLength.md)