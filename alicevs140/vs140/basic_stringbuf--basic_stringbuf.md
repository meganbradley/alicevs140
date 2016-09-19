---
title: "basic_stringbuf::basic_stringbuf"
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
ms.assetid: f722b3a2-5bfe-42a1-9a9a-7e0a2709dcca
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_stringbuf::basic_stringbuf
Constructs an object of type `basic_stringbuf`.  
  
## Syntax  
  
```  
basic_stringbuf(  
    ios_base::openmode _Mode = ios_base::in | ios_base::out  
);  
basic_stringbuf(  
    const basic_string<Elem, Tr, Alloc>& _Str,  
    ios_base::openmode _Mode = ios_base::in | ios_base::out  
);  
```  
  
#### Parameters  
 `_Mode`  
 One of the enumerations in [ios_base::openmode](../vs140/ios_base--openmode.md).  
  
 `_Str`  
 An object of type [basic_string](../vs140/basic_string-Class.md).  
  
## Remarks  
 The first constructor stores a null pointer in all the pointers controlling the input buffer and the output buffer. For more information, see the Remarks section of the [basic_streambuf Class](../vs140/basic_streambuf-Class.md). It also stores `_Mode` as the stringbuf mode. For more information, see the Remarks section of the [basic_stringbuf Class](../vs140/basic_stringbuf-Class.md).  
  
 The second constructor allocates a copy of the sequence controlled by the string object `_Str`. If `_Mode & ios_base::in` is nonzero, it sets the input buffer to start reading at the start of the sequence. If `_Mode & ios_base::out` is nonzero, it sets the output buffer to begin writing at the start of the sequence. It also stores `_Mode` as the stringbuf mode. For more information, see the Remarks section of the [basic_stringbuf Class](../vs140/basic_stringbuf-Class.md).  
  
## Requirements  
 **Header:** <sstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_stringbuf Class](../vs140/basic_stringbuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)