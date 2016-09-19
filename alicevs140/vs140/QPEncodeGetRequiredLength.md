---
title: "QPEncodeGetRequiredLength"
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
ms.assetid: 68652cfd-17f0-45c6-a12a-3a6096ea11e5
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# QPEncodeGetRequiredLength
Call this function to get the size in characters of a buffer that could contain a string encoded from data of the specified size.  
  
## Syntax  
  
```  
  
      inline int QPEncodeGetRequiredLength(  
   int nSrcLen   
) throw( );  
```  
  
#### Parameters  
 `nSrcLen`  
 The number of bytes of data to be encoded.  
  
## Return Value  
 The number of characters required for a buffer that could hold encoded data of `nSrcLen` bytes.  
  
## Remarks  
 The quoted-printable encoding scheme is described in RFC 2045 ([http://www.ietf.org/rfc/rfc2045.txt](http://www.ietf.org/rfc/rfc2045.txt)).  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [QPDecode](../vs140/QPDecode.md)   
 [QPDecodeGetRequiredLength](../vs140/QPDecodeGetRequiredLength.md)   
 [QPEncode](../vs140/QPEncode.md)