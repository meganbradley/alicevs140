---
title: "multi_link_registry::~multi_link_registry Destructor"
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
ms.assetid: d1440277-f5d0-453b-8407-ff17fa9e1866
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multi_link_registry::~multi_link_registry Destructor
Destroys the `multi_link_registry` object.  
  
## Syntax  
  
```  
virtual ~multi_link_registry();  
```  
  
## Remarks  
 The method throws an [invalid_operation](../vs140/invalid_operation-Class.md) exception if called before all links are removed.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [multi_link_registry Class](../vs140/multi_link_registry-Class.md)