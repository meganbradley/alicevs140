---
title: "IDiaFrameData::get_maxStack"
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
ms.assetid: 2585e13c-c0f3-49fe-9a84-08adb0dbeaa4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaFrameData::get_maxStack
Retrieves the maximum number of bytes pushed on the stack in the frame.  
  
## Syntax  
  
```cpp#  
HRESULT get_maxStack (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the maximum number of bytes pushed on the stack.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if this property is not supported. Otherwise, returns an error code.  
  
## Remarks  
 The value returned by this method is typically used in the interpretation of a program string (see the [IDiaFrameData::get_program](../vs140/IDiaFrameData--get_program.md) method for the definition of a program string).  
  
## See Also  
 [IDiaFrameData](../vs140/IDiaFrameData.md)   
 [IDiaFrameData::get_program](../vs140/IDiaFrameData--get_program.md)