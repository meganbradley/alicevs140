---
title: "basic_filebuf::operator="
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
ms.assetid: 0f2bd849-e69e-489b-a9bc-6d8b0151bb65
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_filebuf::operator=
Assign the content of this stream buffer object. This is a move assignment involving an rvalue that does not leave a copy behind.  
  
## Syntax  
  
```  
basic_filebuf& operator=(basic_filebuf&& _Right);  
```  
  
#### Parameters  
 `_Right`  
 An rvalue reference to a [basic_filebuf](../vs140/basic_filebuf-Class.md) object.  
  
## Return Value  
 Returns *this.  
  
## Remarks  
 The member operator replaces the contents of the object by using the contents of `_Right`, treated as an rvalue reference. For more information, see [Rvalue Reference Declarator: &&](../vs140/Rvalue-Reference-Declarator----.md).  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_filebuf Class](../vs140/basic_filebuf-Class.md)   
 [<fstream\>](../vs140/-fstream-.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)