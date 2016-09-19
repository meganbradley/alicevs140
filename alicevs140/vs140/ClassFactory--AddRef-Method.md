---
title: "ClassFactory::AddRef Method"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 5b091785-dea4-42b6-a502-0db5fc7a5a2e
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ClassFactory::AddRef Method
Increments the reference count for the current ClassFactory object.  
  
## Syntax  
  
```  
STDMETHOD_(  
   ULONG,  
   AddRef  
)();  
```  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that describes the failure.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ClassFactory Class](../vs140/ClassFactory-Class.md)