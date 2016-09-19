---
title: "basic_filebuf::basic_filebuf"
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
ms.assetid: 6c3afd9c-32a8-4714-9cec-dc5221ed3524
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_filebuf::basic_filebuf
Constructs an object of type `basic_filebuf`.  
  
## Syntax  
  
```  
basic_filebuf();  
basic_filebuf(basic_filebuf&& right);  
```  
  
## Remarks  
 The first constructor stores a null pointer in all the pointers controlling the input buffer and the output buffer. It also stores a null pointer in the file pointer.  
  
 The second constructor initializes the object with the contents of `right`, treated as an rvalue reference.  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_filebuf Class](../vs140/basic_filebuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)