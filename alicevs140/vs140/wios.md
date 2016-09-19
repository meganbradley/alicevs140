---
title: "wios"
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
ms.assetid: 49ba32b6-05bd-4b29-9d4d-f6bd44fed09a
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# wios
Supports the wios class from the old iostream library.  
  
## Syntax  
  
```  
  
typedef basic  
_  
ios<wchar  
_  
t, char  
_  
traits<wchar  
_  
t> > wios;  
  
```  
  
## Remarks  
 The type is a synonym for template class [basic_ios](../vs140/basic_ios-Class.md), specialized for elements of type `wchar_t` with default character traits.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ios Class](../vs140/basic_ios-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)