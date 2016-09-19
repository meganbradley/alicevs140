---
title: "AtlHexEncode"
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
ms.assetid: 256f1d5c-ca40-488e-bcfb-503cf6ac0ea8
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlHexEncode
Call this function to encode some data as a string of hexadecimal text.  
  
## Syntax  
  
```  
  
      inline BOOL AtlHexEncode(  
   const BYTE * pbSrcData,  
   int nSrcLen,  
   LPSTR szDest,  
   int * pnDestLen   
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
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 Each byte of source data is encoded as 2 hexadecimal characters.  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [AtlHexDecodeGetRequiredLength](../vs140/AtlHexDecodeGetRequiredLength.md)   
 [AtlHexDecode](../vs140/AtlHexDecode.md)   
 [AtlHexEncodeGetRequiredLength](../vs140/AtlHexEncodeGetRequiredLength.md)