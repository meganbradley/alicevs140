---
title: "IDiaFrameData::get_lengthParams"
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
ms.assetid: a9177ed6-9ba8-4384-b411-24cad07d031b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaFrameData::get_lengthParams
Retrieves the number of bytes of parameters pushed on the stack.  
  
## Syntax  
  
```cpp#  
HRESULT get_lengthParams (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the number of bytes of parameters.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if this property is not supported. Otherwise, returns an error code.  
  
## Remarks  
 The value returned by this method is typically used in the interpretation of a program string (see the [IDiaFrameData::get_program](../vs140/IDiaFrameData--get_program.md) method for the definition of a program string).  
  
## See Also  
 [IDiaFrameData](../vs140/IDiaFrameData.md)   
 [IDiaFrameData::get_program](../vs140/IDiaFrameData--get_program.md)