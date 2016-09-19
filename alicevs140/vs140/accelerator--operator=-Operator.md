---
title: "accelerator::operator= Operator"
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
ms.assetid: 66e2f395-9000-4e4c-be53-ccf1188753ed
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# accelerator::operator= Operator
Copies the contents of the specified [accelerator](../vs140/accelerator-Class.md) object to this one.  
  
## Syntax  
  
```  
accelerator &operator=(  
   const accelerator &_Other                       
);  
```  
  
#### Parameters  
 `_Other`  
 The `accelerator` object to copy from.  
  
## Return Value  
 A reference to this `accelerator` object.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [accelerator Class](../vs140/accelerator-Class.md)