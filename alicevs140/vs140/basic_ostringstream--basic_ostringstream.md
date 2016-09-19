---
title: "basic_ostringstream::basic_ostringstream"
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
ms.assetid: e8c85a0a-0cc5-4395-8786-f754e3b65992
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ostringstream::basic_ostringstream
Constructs an object of type basic_ostringstream.  
  
## Syntax  
  
```  
  
      explicit basic  
      _  
      ostringstream(  
   ios_base::openmode _Mode = ios_base::out  
);  
explicit basic_ostringstream(  
   const basic_string<Elem, Tr, Alloc>& _Str,  
   ios_base::openmode _Mode = ios_base::out  
);  
```  
  
#### Parameters  
 `_Mode`  
 One of the enumerations in [ios_base::openmode](../vs140/ios_base--openmode.md).  
  
 `_Str`  
 An object of type `basic_string`.  
  
## Remarks  
 The first constructor initializes the base class by calling [basic_ostream](../vs140/basic_ostream-Class.md)(**sb**), where **sb** is the stored object of class [basic_stringbuf](../vs140/basic_stringbuf-Class.md)<**Elem**, **Tr**, `Alloc`>. It also initializes **sb** by calling basic_stringbuf<**Elem**, **Tr**, `Alloc`>(`_Mode` &#124; `ios_base::out`).  
  
 The second constructor initializes the base class by calling basic_ostream(**sb**). It also initializes **sb** by calling basic_stringbuf<**Elem**, **Tr**, `Alloc`>(_*Str*, `_Mode` &#124; `ios_base::out`).  
  
## Requirements  
 **Header:** <sstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ostringstream Class](../vs140/basic_ostringstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)