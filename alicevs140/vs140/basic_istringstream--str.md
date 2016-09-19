---
title: "basic_istringstream::str"
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
ms.assetid: 2cce3757-a9ff-4f2c-826c-337895b99384
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_istringstream::str
Sets or gets the text in a string buffer without changing the write position.  
  
## Syntax  
  
```  
basic_string<Elem, Tr, Alloc> str( ) const;  
void str(  
    const basic_string<Elem, Tr, Alloc>& _Newstr  
);  
```  
  
#### Parameters  
 `_Newstr`  
 The new string.  
  
## Return Value  
 Returns an object of class [basic_string](../vs140/basic_string-Class.md)<**Elem**, **Tr**, `Alloc`>, whose controlled sequence is a copy of the sequence controlled by **\*this**.  
  
## Remarks  
 The first member function returns [rdbuf](../vs140/basic_istringstream--rdbuf.md) -> [str](../vs140/basic_stringbuf--str.md). The second member function calls `rdbuf` -> **str**(`_Newstr`).  
  
## Example  
 See [basic_stringbuf::str](../vs140/basic_stringbuf--str.md) for an example that uses **str**.  
  
## Requirements  
 **Header:** <sstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_istringstream Class](../vs140/basic_istringstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)