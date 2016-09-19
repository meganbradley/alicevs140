---
title: "UUDecodeGetRequiredLength"
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
ms.assetid: abfa1d1f-caf6-4029-a94c-1a48937791dd
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# UUDecodeGetRequiredLength
Call this function to get the size in bytes of a buffer that could contain data decoded from a uuencoded string of the specified length.  
  
## Syntax  
  
```  
  
      inline int UUDecodeGetRequiredLength(  
   int nSrcLen   
) throw( );  
```  
  
#### Parameters  
 `nSrcLen`  
 The number of characters in the encoded string.  
  
## Return Value  
 The number of bytes required for a buffer that could hold a decoded string of `nSrcLen` characters.  
  
## Remarks  
 This uuencoding implementation follows the POSIX P1003.2b/D11 specification.  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [UUDecode](../vs140/UUDecode.md)   
 [UUEncode](../vs140/UUEncode.md)   
 [UUEncodeGetRequiredLength](../vs140/UUEncodeGetRequiredLength.md)