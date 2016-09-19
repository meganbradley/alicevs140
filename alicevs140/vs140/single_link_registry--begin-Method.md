---
title: "single_link_registry::begin Method"
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
ms.assetid: daf5cd92-e76a-4dd2-ac53-26fe5b373d89
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# single_link_registry::begin Method
Returns an iterator to the first element in the `single_link_registry` object.  
  
## Syntax  
  
```  
virtual iterator begin();  
```  
  
## Return Value  
 An iterator addressing the first element in the `single_link_registry` object.  
  
## Remarks  
 The end state is indicated by a `NULL` link.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [single_link_registry Class](../vs140/single_link_registry-Class.md)