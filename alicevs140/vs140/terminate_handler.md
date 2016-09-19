---
title: "terminate_handler"
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
ms.assetid: a820e7c0-ef5b-46e2-8823-e0de4e5c2e6c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# terminate_handler
The type describes a pointer to a function suitable for use as a `terminate_handler`.  
  
## Syntax  
  
```  
  
typedef void ( *terminate_handler )( );  
  
```  
  
## Remarks  
 The type describes a pointer to a function suitable for use as a terminate handler.  
  
## Example  
 See [set_terminate](../vs140/set_terminate---exception--.md) for an example of the use of `terminate_handler`.  
  
## Requirements  
 **Header:** <exception\>  
  
 **Namespace:** std