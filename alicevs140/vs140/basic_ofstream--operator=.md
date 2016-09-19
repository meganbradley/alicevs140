---
title: "basic_ofstream::operator="
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
ms.assetid: 15ce7854-f874-4246-ad9a-21f05ca9ed7a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ofstream::operator=
Assigns the content of this stream object. This is a move assignment involving an `rvalue reference` that does not leave a copy behind.  
  
## Syntax  
  
```  
basic_ofstream& operator=(  
    basic_ofstream&& _Right  
);  
```  
  
#### Parameters  
 `_Right`  
 An rvalue reference to a `basic_ofstream` object.  
  
## Return Value  
 Returns `*this`.  
  
## Exceptions  
  
## Remarks  
 The member operator replaces the contents of the object by using the contents of `_Right`, treated as an rvalue reference.  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ofstream Class](../vs140/basic_ofstream-Class.md)   
 [<fstream\>](../vs140/-fstream-.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)