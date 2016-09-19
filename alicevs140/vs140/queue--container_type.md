---
title: "queue::container_type"
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
ms.assetid: 3f1f1c34-a2d1-4406-9b6e-ba26db902f9e
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# queue::container_type
A type that provides the base container to be adapted.  
  
## Syntax  
  
```  
  
typedef Container container_type;  
```  
  
## Remarks  
 The type is a synonym for the template parameter `Container`. Two STL sequence container classes — the list class and the default deque class — meet the requirements to be used as the base container for a queue object. User-defined types satisfying the requirements may also be used.  
  
 For more information on `Container`, see the Remarks section of the [queue Class](../vs140/queue-Class.md) topic.  
  
## Example  
 See the example for [queue](../vs140/queue--queue.md) for an example of how to declare and use `container_type`.  
  
## Requirements  
 **Header:** <queue\>  
  
 **Namespace:** std  
  
## See Also  
 [queue Class](../vs140/queue-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)