---
title: "QEncode"
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
ms.assetid: 6dba5385-ecfc-4a18-85ab-4e8a224384f9
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# QEncode
Call this function to convert some data using the "Q" encoding.  
  
## Syntax  
  
```  
  
      inline BOOL QEncode(  
   BYTE* pbSrcData,  
   int nSrcLen,  
   LPSTR szDest,  
   int* pnDestLen,  
   LPCSTR pszCharSet,  
   int* pnNumEncoded = NULL   
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
  
 `pszCharSet`  
 The character set to use for the conversion.  
  
 *pnNumEncoded*  
 A pointer to a variable that on return contains the number of unsafe characters that had to be converted.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 The "Q" encoding scheme is described in RFC 2047 ([http://www.ietf.org/rfc/rfc2047.txt](http://www.ietf.org/rfc/rfc2047.txt)).  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [QEncodeGetRequiredLength](../vs140/QEncodeGetRequiredLength.md)