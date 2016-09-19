---
title: "basic_ostringstream::rdbuf"
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
ms.assetid: e55c6eb7-b717-4679-b348-c005b6c8f55d
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ostringstream::rdbuf
Returns the address of the stored stream buffer of type **pointer** to [basic_stringbuf](../vs140/basic_stringbuf-Class.md)<**Elem**, **Tr**, `Alloc`>.  
  
## Syntax  
  
```  
basic_stringbuf<Elem, Tr, Alloc> *rdbuf( ) const;  
```  
  
## Return Value  
 The address of the stored stream buffer, of type **pointer** to basic_stringbuf<**Elem**, **Tr**, `Alloc`>.  
  
## Remarks  
 The member function returns the address of the stored stream buffer of type **pointer** to basic_stringbuf<**Elem**, **Tr**, `Alloc`>.  
  
## Example  
 See [basic_filebuf::close](../vs140/basic_filebuf--close.md) for an example that uses `rdbuf`.  
  
## Requirements  
 **Header:** <sstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ostringstream Class](../vs140/basic_ostringstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)