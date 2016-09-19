---
title: "AtlHexDecode"
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
ms.assetid: 305ccc56-7f96-4795-b297-b04e58c98187
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlHexDecode
Decodes a string of data that has been encoded as hexadecimal text such as by a previous call to [AtlHexEncode](../vs140/AtlHexEncode.md).  
  
## Syntax  
  
```  
  
      inline BOOL AtlHexDecode(  
   LPCSTR pSrcData,  
   int nSrcLen,  
   LPBYTE pbDest,  
   int* pnDestLen   
) throw( );  
```  
  
#### Parameters  
 `pSrcData`  
 The string containing the data to be decoded.  
  
 `nSrcLen`  
 The length in characters of `pSrcData`.  
  
 `pbDest`  
 Caller-allocated buffer to receive the decoded data.  
  
 `pnDestLen`  
 Pointer to a variable that contains the length in bytes of `pbDest`. If the function succeeds, the variable receives the number of bytes written to the buffer. If the function fails, the variable receives the required length in bytes of the buffer.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [AtlHexDecodeGetRequiredLength](../vs140/AtlHexDecodeGetRequiredLength.md)   
 [AtlHexEncode](../vs140/AtlHexEncode.md)   
 [AtlHexEncodeGetRequiredLength](../vs140/AtlHexEncodeGetRequiredLength.md)