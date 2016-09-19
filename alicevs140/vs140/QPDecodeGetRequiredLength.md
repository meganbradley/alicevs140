---
title: "QPDecodeGetRequiredLength"
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
ms.assetid: 84750f57-75c3-4c0d-bcfa-57a55d034198
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# QPDecodeGetRequiredLength
Call this function to get the size in bytes of a buffer that could contain data decoded from quoted-printable-encoded string of the specified length.  
  
## Syntax  
  
```  
  
      inline int QPDecodeGetRequiredLength(  
   int nSrcLen   
) throw( );  
```  
  
#### Parameters  
 `nSrcLen`  
 The number of characters in the encoded string.  
  
## Return Value  
 The number of bytes required for a buffer that could hold a decoded string of `nSrcLen` characters.  
  
## Remarks  
 The quoted-printable encoding scheme is described in RFC 2045 ([http://www.ietf.org/rfc/rfc2045.txt](http://www.ietf.org/rfc/rfc2045.txt)).  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [QPDecode](../vs140/QPDecode.md)   
 [QPEncode](../vs140/QPEncode.md)   
 [QPEncodeGetRequiredLength](../vs140/QPEncodeGetRequiredLength.md)