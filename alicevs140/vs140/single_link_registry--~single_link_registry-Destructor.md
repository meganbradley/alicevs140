---
title: "single_link_registry::~single_link_registry Destructor"
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
ms.assetid: 33410fa9-c4f2-40e0-b604-93b993601d1b
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# single_link_registry::~single_link_registry Destructor
Destroys the `single_link_registry` object.  
  
## Syntax  
  
```  
virtual ~single_link_registry();  
```  
  
## Remarks  
 The method throws an [invalid_operation](../vs140/invalid_operation-Class.md) exception if it is called before the link is removed.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [single_link_registry Class](../vs140/single_link_registry-Class.md)