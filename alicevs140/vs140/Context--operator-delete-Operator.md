---
title: "Context::operator delete Operator"
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
ms.topic: article
ms.assetid: 3d01275c-907b-4503-852a-5df7494150d8
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Context::operator delete Operator
A `Context` object is destroyed internally by the runtime. It can not be explicitly deleted.  
  
## Syntax  
  
```  
void operator delete(  
   void * _PObject  
);  
```  
  
#### Parameters  
 `_PObject`  
 A pointer to the object to be deleted.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Context Class](../vs140/Context-Class.md)