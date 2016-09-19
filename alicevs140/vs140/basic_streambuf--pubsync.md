---
title: "basic_streambuf::pubsync"
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
ms.assetid: 5d45ebdf-de99-4673-9eba-e386a8ae415e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::pubsync
Calls [sync](../vs140/basic_streambuf--sync.md), a protected virtual function that is overridden in a derived class, and updates the external stream associated with this buffer.  
  
## Syntax  
  
```  
  
int pubsync( );  
  
```  
  
## Return Value  
 Returns [sync](../vs140/basic_streambuf--sync.md) or –1 if failure.  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)