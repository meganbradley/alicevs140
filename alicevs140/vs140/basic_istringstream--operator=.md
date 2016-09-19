---
title: "basic_istringstream::operator="
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
ms.assetid: 74026b4a-2fe7-41aa-ae90-c6379a41c3c1
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# basic_istringstream::operator=
Assigns the values to this `basic_istringstream` object from the object parameter.  
  
## Syntax  
  
```  
basic_istringstream& operator=(  
    basic_istringstream&& _Right  
);  
```  
  
#### Parameters  
 `_Right`  
 An rvalue reference to a `basic_istringstream` object.  
  
## Property Value/Return Value  
  
## Remarks  
 The member operator replaces the contents of the object with the contents of `_Right`, treated as an rvalue reference move assignment.  
  
## Requirements  
 **Header:** <sstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_istringstream Class](../vs140/basic_istringstream-Class.md)   
 [<sstream\>](../vs140/-sstream-.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)