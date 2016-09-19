---
title: "basic_istringstream::basic_istringstream"
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
ms.assetid: d38deb70-ff11-416a-add4-f266d04e10df
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_istringstream::basic_istringstream
Constructs an object of type `basic_istringstream`.  
  
## Syntax  
  
```  
explicit basic_istringstream(  
   ios_base::openmode _Mode = ios_base::in  
);  
explicit basic_istringstream(  
   const basic_string<Elem, Tr, Alloc>& _Str,  
   ios_base::openmode _Mode = ios_base::in  
);  
basic_istringstream(  
    basic_istringstream&& _Right  
);  
```  
  
#### Parameters  
 `_Mode`  
 One of the enumerations in [ios_base::openmode](../vs140/ios_base--openmode.md).  
  
 `_Str`  
 An object of type `basic_string`.  
  
 `_Right`  
 An rvalue reference of a `basic_istringstream` object.  
  
## Remarks  
 The first constructor initializes the base class by calling [basic_istream](../vs140/basic_istream-Class.md)(`sb`), where `sb` is the stored object of class [basic_stringbuf](../vs140/basic_stringbuf-Class.md)<`Elem`, `Tr`, `Alloc`>. It also initializes `sb` by calling `basic_stringbuf`<`Elem`, `Tr`, `Alloc`>(`_Mode` &#124; `ios_base::in`).  
  
 The second constructor initializes the base class by calling `basic_istream(sb)`. It also initializes `sb` by calling `basic_stringbuf`<`Elem`, `Tr`, `Alloc`>(`_Str`, `_Mode` &#124; `ios_base::in`).  
  
 The third constructor initializes the object with the contents of `_Right`, treated as an rvalue reference.  
  
## Requirements  
 **Header:** <sstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_istringstream Class](../vs140/basic_istringstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)