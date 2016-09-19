---
title: "array::get_accelerator_view Method"
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
ms.assetid: fc06031a-4a3b-4869-acae-05f219022832
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array::get_accelerator_view Method
Returns the [accelerator_view](../vs140/accelerator_view-Class.md) object that represents the location where the [array](../vs140/array-Class.md) object is allocated. This property can be accessed only on the CPU.  
  
## Syntax  
  
```  
Concurrency::accelerator_view get_accelerator_view() const;  
```  
  
## Return Value  
 The `accelerator_view` object that represents the location where the [array](../vs140/array-Class.md) object is allocated.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [array Class](../vs140/array-Class.md)