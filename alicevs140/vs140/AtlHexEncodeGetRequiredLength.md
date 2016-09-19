---
title: "AtlHexEncodeGetRequiredLength"
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
ms.assetid: 7decfd9b-7227-4676-b16f-f50ffc6c0caa
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlHexEncodeGetRequiredLength
Call this function to get the size in characters of a buffer that could contain a string encoded from data of the specified size.  
  
## Syntax  
  
```  
  
      inline int AtlHexEncodeGetRequiredLength(  
   int nSrcLen   
) throw( );  
```  
  
#### Parameters  
 `nSrcLen`  
 The number of bytes of data to be encoded.  
  
## Return Value  
 The number of characters required for a buffer that could hold encoded data of `nSrcLen` bytes.  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [AtlHexDecodeGetRequiredLength](../vs140/AtlHexDecodeGetRequiredLength.md)   
 [AtlHexEncode](../vs140/AtlHexEncode.md)   
 [AtlHexDecode](../vs140/AtlHexDecode.md)