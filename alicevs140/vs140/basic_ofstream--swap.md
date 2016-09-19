---
title: "basic_ofstream::swap"
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
ms.assetid: e0c90696-4d58-4c4a-b7df-34e2ab97b921
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# basic_ofstream::swap
Exchanges the contents of two `basic_ofstream` objects.  
  
## Syntax  
  
```  
void swap(  
    basic_ofstream& _Right  
);  
```  
  
#### Parameters  
 `_Right`  
 An `lvalue` reference to another `basic_ofstream` object.  
  
## Remarks  
 The member function exchanges the contents of this object for the contents of `_Right`.  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ofstream Class](../vs140/basic_ofstream-Class.md)   
 [basic_ostream Class](../vs140/basic_ostream-Class.md)   
 [<fstream\>](../vs140/-fstream-.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)   
 [Thread Safety in the C++ Standard Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)