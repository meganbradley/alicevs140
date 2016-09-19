---
title: "unexpected_handler"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 33e1efdd-6653-4990-925c-77df9f5325d1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unexpected_handler
The type describes a pointer to a function suitable for use as an `unexpected_handler`.  
  
## Syntax  
  
```  
  
typedef void (*unexpected_handler)( );  
  
```  
  
## Example  
 See [set_unexpected](../vs140/set_unexpected---exception--.md) for an example of the use of `unexpected_handler`.  
  
## Requirements  
 **Header:** <exception\>  
  
 **Namespace:** std