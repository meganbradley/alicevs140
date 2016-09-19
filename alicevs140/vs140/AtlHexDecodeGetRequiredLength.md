---
title: "AtlHexDecodeGetRequiredLength"
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
ms.assetid: d2a28877-fe5e-420d-93b4-3b46d910d752
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlHexDecodeGetRequiredLength
Call this function to get the size in bytes of a buffer that could contain data decoded from a hex-encoded string of the specified length.  
  
## Syntax  
  
```  
  
      inline int AtlHexDecodeGetRequiredLength(  
   int nSrcLen   
) throw( );  
```  
  
#### Parameters  
 `nSrcLen`  
 The number of characters in the encoded string.  
  
## Return Value  
 The number of bytes required for a buffer that could hold a decoded string of `nSrcLen` characters.  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [AtlHexDecode](../vs140/AtlHexDecode.md)   
 [AtlHexEncode](../vs140/AtlHexEncode.md)   
 [AtlHexEncodeGetRequiredLength](../vs140/AtlHexEncodeGetRequiredLength.md)