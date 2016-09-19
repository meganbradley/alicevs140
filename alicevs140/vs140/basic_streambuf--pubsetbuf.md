---
title: "basic_streambuf::pubsetbuf"
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
ms.assetid: f26de46b-0e78-45bb-a6cd-c6b58704c4f8
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::pubsetbuf
Calls [setbuf](../vs140/basic_streambuf--setbuf.md), a protected virtual function that is overridden in a derived class.  
  
## Syntax  
  
```  
basic_streambuf<Elem, Tr> *pubsetbuf(  
    char_type *_Buffer,  
    streamsize _Count  
);  
```  
  
#### Parameters  
 `_Buffer`  
 A pointer to `char_type` for this instantiation.  
  
 `_Count`  
 The size of the buffer.  
  
## Return Value  
 Returns [setbuf](../vs140/basic_streambuf--setbuf.md)(`_Buffer`, `_Count`).  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)