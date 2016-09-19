---
title: "network_link_registry::begin Method"
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
ms.assetid: 9c801361-ebbd-4cef-9aaf-6d5ad0a869e7
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# network_link_registry::begin Method
When overridden in a derived class, returns an iterator to the first element in the `network_link_registry` object.  
  
## Syntax  
  
```  
virtual iterator begin() = 0;  
```  
  
## Return Value  
 An iterator addressing the first element in the `network_link_registry` object.  
  
## Remarks  
 The end state of the iterator is indicated by a `NULL` link.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [network_link_registry Class](../vs140/network_link_registry-Class.md)