---
title: "array::get_associated_accelerator_view Method"
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
ms.assetid: 2756737e-29a9-4721-8205-e8a945253ae8
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array::get_associated_accelerator_view Method
Gets the second [accelerator_view](../vs140/accelerator_view-Class.md) object that is passed as a parameter when a staging constructor is called to instantiate the  [array](../vs140/array-Class.md) object.  
  
## Syntax  
  
```  
Concurrency::accelerator_view get_associated_accelerator_view() const ;  
```  
  
## Return Value  
 The second [accelerator_view](../vs140/accelerator_view-Class.md) object passed to the staging constructor.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [array Class](../vs140/array-Class.md)