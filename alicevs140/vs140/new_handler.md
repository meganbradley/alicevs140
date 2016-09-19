---
title: "new_handler"
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
ms.assetid: 4a28059f-a15a-478c-a63f-7dff446574e4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# new_handler
The type points to a function suitable for use as a new handler.  
  
## Syntax  
  
```  
  
typedef void ( *new_handler )( );  
  
```  
  
## Remarks  
 This type of handler function is called by **operator new** or `operator new[]` when they cannot satisfy a request for additional storage.  
  
## Example  
 See [set_new_handler](../vs140/set_new_handler.md) for an example using `new_handler` as a return value.  
  
## Requirements  
 **Header:** <new\>  
  
 **Namespace:** std