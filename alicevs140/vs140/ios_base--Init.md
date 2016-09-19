---
title: "ios_base::Init"
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
ms.assetid: f78b9732-f3f9-4c28-a6fa-f214c14d7e24
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ios_base::Init
Creates the standard iostream objects when constructed.  
  
## Syntax  
  
```  
  
class Init { };  
  
```  
  
## Remarks  
 The nested class describes an object whose construction ensures that the standard iostreams objects are properly constructed, even before the execution of a constructor for an arbitrary static object.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [ios_base Class](../vs140/ios_base-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)