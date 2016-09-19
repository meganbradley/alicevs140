---
title: "HandleT::InternalClose Method"
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
ms.assetid: fe693c02-aa1f-4e00-8bdd-a0d7d736da0b
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HandleT::InternalClose Method
Closes the current HandleT object.  
  
## Syntax  
  
```  
virtual bool InternalClose();  
```  
  
## Return Value  
 `true` if the current HandleT closed successfully; otherwise, `false`.  
  
## Remarks  
 InternalClose() is protected.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [HandleT Class](../vs140/HandleT-Class.md)