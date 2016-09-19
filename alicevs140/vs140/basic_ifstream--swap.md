---
title: "basic_ifstream::swap"
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
ms.assetid: 6edefa43-4ec0-4df8-8976-e9a9203736a6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# basic_ifstream::swap
Exchanges the contents of two `basic_ifstream` objects.  
  
## Syntax  
  
```  
void swap(  
    basic_ifstream& _Right  
);  
```  
  
#### Parameters  
 `_Right`  
 A reference to another stream buffer.  
  
## Remarks  
 The member function exchanges the contents of this object for the contents of `_Right`.  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ifstream Class](../vs140/basic_ifstream-Class.md)   
 [<fstream\>](../vs140/-fstream-.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)