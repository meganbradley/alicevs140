---
title: "ClassFactory::LockServer Method"
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
ms.assetid: 8d859815-956d-4f81-a5af-7cdee7e945de
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ClassFactory::LockServer Method
Increments or decrements the number of underlying objects that are tracked by the current ClassFactory object.  
  
## Syntax  
  
```  
STDMETHOD(  
   LockServer  
)(BOOL fLock);  
```  
  
#### Parameters  
 `fLock`  
 `true` to increment the number of tracked objects. `false` to decrement the number of tracked objects.  
  
## Return Value  
 S_OK if successful; otherwise, E_FAIL.  
  
## Remarks  
 ClassFactory keeps track of objects in an underlying instance of the [Module](../vs140/Module-Class.md) class.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ClassFactory Class](../vs140/ClassFactory-Class.md)