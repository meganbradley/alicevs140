---
title: "wstreambuf"
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
ms.assetid: b9f1b7bb-63e4-46d2-baaf-bf41b747da8b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# wstreambuf
A specialization of `basic_streambuf` that uses `wchar_t` as the template parameters.  
  
## Syntax  
  
```  
  
typedef basic  
_  
streambuf<wchar  
_  
t, char  
_  
traits<wchar  
_  
t> > wstreambuf;  
  
```  
  
## Remarks  
 The type is a synonym for the template class [basic_streambuf](../vs140/basic_streambuf-Class.md), specialized for elements of type `wchar_t` with default character traits.  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)