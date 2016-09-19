---
title: "basic_filebuf::sync"
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
ms.assetid: a2ebb2b1-6bf0-4716-9a61-6691403dbd37
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_filebuf::sync
Tries to synchronize the controlled streams with any associated external streams.  
  
## Syntax  
  
```  
virtual int sync( );  
```  
  
## Return Value  
 Returns zero if the file pointer **fp** is a null pointer. Otherwise, it returns zero only if calls to both [overflow](../vs140/basic_filebuf--overflow.md) and `fflush`(**fp**) succeed in flushing any pending output to the stream.  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_filebuf Class](../vs140/basic_filebuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)