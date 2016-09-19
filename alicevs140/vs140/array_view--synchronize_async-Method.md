---
title: "array_view::synchronize_async Method"
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
ms.assetid: c9a41b8e-9e71-44e8-b785-e1b7c46279ff
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array_view::synchronize_async Method
Asynchronously synchronizes any modifications made to the [array_view](../vs140/array_view-Class.md) object back to its source data.  
  
## Syntax  
  
```  
concurrency::completion_future synchronize_async(  
   access_type _Access_type = access_type_read  
) const restrict(cpu);  
  
concurrency::completion_future synchronize_async() const restrict(cpu);  
```  
  
#### Parameters  
 `_Access_type`  
 The intended [access_type](../vs140/access_type-Enumeration.md) on the target [accelerator_view](../vs140/accelerator_view-Class.md). This parameter has a default value of `access_type_read`.  
  
## Return Value  
 A future upon which to wait for the operation to complete.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [array_view Class](../vs140/array_view-Class.md)