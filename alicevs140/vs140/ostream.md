---
title: "ostream"
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
ms.assetid: 149eb412-a60a-4baf-a9df-99beab5c91dc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ostream
Creates a type from basic_ostream that is specialized on `char` and `char_traits` specialized on `char`.  
  
## Syntax  
  
```  
  
typedef basic  
_  
ostream<char, char  
_  
traits<char> > ostream;  
  
```  
  
## Remarks  
 The type is a synonym for template class [basic_ostream](../vs140/basic_ostream-Class.md), specialized for elements of type `char` with default character traits.  
  
## Requirements  
 **Header:** <ostream\>  
  
 **Namespace:** std  
  
## See Also  
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)