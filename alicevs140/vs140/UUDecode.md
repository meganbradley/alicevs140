---
title: "UUDecode"
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
ms.assetid: 5841f625-166f-4f4a-a4f8-841982fa7a22
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# UUDecode
Decodes a string of data that has been uuencoded such as by a previous call to [UUEncode](../vs140/UUEncode.md).  
  
## Syntax  
  
```  
  
      inline BOOL UUDecode(  
   BYTE* pbSrcData,  
   int nSrcLen,  
   BYTE* pbDest,  
   int* pnDestLen   
) throw( );  
```  
  
#### Parameters  
 `pbSrcData`  
 The string containing the data to be decoded.  
  
 `nSrcLen`  
 The length in bytes of `pbSrcData`.  
  
 `pbDest`  
 Caller-allocated buffer to receive the decoded data.  
  
 `pnDestLen`  
 Pointer to a variable that contains the length in bytes of `pbDest`. If the function succeeds, the variable receives the number of bytes written to the buffer. If the function fails, the variable receives the required length in bytes of the buffer.  
  
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
 [UUDecodeGetRequiredLength](../vs140/UUDecodeGetRequiredLength.md)   
 [UUEncode](../vs140/UUEncode.md)   
 [UUEncodeGetRequiredLength](../vs140/UUEncodeGetRequiredLength.md)