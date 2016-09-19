---
title: "accelerator_view::operator= Operator"
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
ms.assetid: ac4aa0a2-6da9-4aea-a2e0-06b81abb81ab
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# accelerator_view::operator= Operator
Copies the contents of the specified  [accelerator_view](../vs140/accelerator_view-Class.md) object into this one.  
  
## Syntax  
  
```  
accelerator_view &operator=(  
   const accelerator_view &_Other                       
);  
```  
  
#### Parameters  
 `_Other`  
 The `accelerator_view` object to copy from.  
  
## Return Value  
 A reference to the modified `accelerator_view` object.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [accelerator_view Class](../vs140/accelerator_view-Class.md)