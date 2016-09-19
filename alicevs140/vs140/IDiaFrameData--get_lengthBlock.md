---
title: "IDiaFrameData::get_lengthBlock"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2e54deb7-7744-428e-913c-1d47a2aa89b0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaFrameData::get_lengthBlock
Retrieves the length, in bytes, of the block of code described by the frame.  
  
## Syntax  
  
```cpp#  
HRESULT get_lengthBlock (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the number of bytes of code in the frame.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if this property is not supported. Otherwise, returns an error code.  
  
## Remarks  
 The value returned by this method is typically used in the interpretation of a program string (see the [IDiaFrameData::get_program](../vs140/IDiaFrameData--get_program.md) method for the definition of a program string).  
  
## See Also  
 [IDiaFrameData](../vs140/IDiaFrameData.md)   
 [IDiaFrameData::get_program](../vs140/IDiaFrameData--get_program.md)