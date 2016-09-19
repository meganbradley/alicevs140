---
title: "basic_stringstream::basic_stringstream"
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
ms.assetid: 2ea524e7-62d5-480e-9ed8-972abed7b4c8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_stringstream::basic_stringstream
Constructs an object of type `basic_stringstream`.  
  
## Syntax  
  
```  
  
      explicit basic  
      _  
      stringstream(  
   ios_base::openmode _Mode = ios_base::in | ios_base::out  
);  
explicit basic_stringstream(  
   const basic_string<Elem, Tr, Alloc>& _Str,  
   ios_base::openmode _Mode = ios_base::in | ios_base::out  
);  
```  
  
#### Parameters  
 `_Mode`  
 One of the enumerations in [ios_base::openmode](../vs140/ios_base--openmode.md).  
  
 `_Str`  
 An object of type `basic_string`.  
  
## Remarks  
 The first constructor initializes the base class by calling [basic_iostream](../vs140/basic_iostream-Class.md)(**sb**), where **sb** is the stored object of class [basic_stringbuf](../vs140/basic_stringbuf-Class.md)<**Elem**, **Tr**, `Alloc`>. It also initializes **sb** by calling basic_stringbuf<**Elem**, **Tr**, `Alloc`>(`_Mode`).  
  
 The second constructor initializes the base class by calling basic_iostream(**sb**). It also initializes **sb** by calling basic_stringbuf<**Elem**, **Tr**, `Alloc`>(_*Str*, `_Mode`).  
  
## Requirements  
 **Header:** <sstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_stringstream Class](../vs140/basic_stringstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)