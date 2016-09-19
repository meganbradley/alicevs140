---
title: "wiostream"
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
ms.assetid: 300a4ec7-56c7-48d5-ad58-805d4e6edbf9
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# wiostream
A type `basic_iostream` specialized on `wchar_t`.  
  
## Syntax  
  
```  
  
typedef basic  
_  
iostream<wchar  
_  
t, char  
_  
traits<wchar  
_  
t> > wiostream;  
  
```  
  
## Remarks  
 The type is a synonym for template class [basic_iostream](../vs140/basic_iostream-Class.md), specialized for elements of type `wchar_t` with default character traits.  
  
## Requirements  
 **Header:** <istream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_iostream Class](../vs140/basic_iostream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)