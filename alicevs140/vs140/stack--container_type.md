---
title: "stack::container_type"
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
ms.assetid: 2b877bb6-d884-408c-b625-d2d6b6121332
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# stack::container_type
A type that provides the base container to be adapted.  
  
## Syntax  
  
```  
  
typedef Container container_type;  
```  
  
## Remarks  
 The type is a synonym for the template parameter `Container`. All three STL sequence container classes — the vector class, list class, and the default class deque — meet the requirements to be used as the base container for a stack object. User-defined types satisfying these requirements may also be used.  
  
 For more information on `Container`, see the Remarks section of the [stack Class](../vs140/stack-Class.md) topic.  
  
## Example  
 See the example for [stack::stack](../vs140/stack--stack.md) for an example of how to declare and use `container_type`.  
  
## Requirements  
 **Header:** <stack\>  
  
 **Namespace:** std  
  
## See Also  
 [stack Class](../vs140/stack-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)