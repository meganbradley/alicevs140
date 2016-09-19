---
title: "basic_fstream::swap"
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
ms.assetid: 24a986bf-fcde-4fb0-9c9b-3620bcea63b3
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_fstream::swap
Exchanges the contents of two `basic_fstream` objects.  
  
## Syntax  
  
```  
void swap(basic_fstream& _Right);  
```  
  
#### Parameters  
 `_Right`  
 An `lvalue` reference to a `basic_fstream` object.  
  
## Remarks  
 The member function exchanges the contents of this object and the contents of `_Right`.  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_fstream Class](../vs140/basic_fstream-Class.md)   
 [<fstream\>](../vs140/-fstream-.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)