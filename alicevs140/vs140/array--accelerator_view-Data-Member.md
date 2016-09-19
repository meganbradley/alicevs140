---
title: "array::accelerator_view Data Member"
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
ms.assetid: 13f04d13-ab25-437e-8213-711377d3a701
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array::accelerator_view Data Member
Gets the [accelerator_view](../vs140/accelerator_view-Class.md) object that represents the location where the array is allocated. This property can be accessed only on the CPU.  
  
## Syntax  
  
```  
__declspec(property(get=get_accelerator_view)) Concurrency::accelerator_view accelerator_view;  
```  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [array Class](../vs140/array-Class.md)