---
title: "Character Sequences"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1e6961a9-150e-4c13-b427-9af4b6a1fb7a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Character Sequences
**ANSI 3.8.2** The mapping of source file character sequences  
  
 Preprocessor statements use the same character set as source file statements with the exception that escape sequences are not supported.  
  
 Thus, to specify a path for an include file, use only one backslash:  
  
```  
#include "path1\path2\myfile"  
```  
  
 Within source code, two backslashes are necessary:  
  
```  
fil = fopen( "path1\\path2\\myfile", "rt" );  
```  
  
## See Also  
 [Preprocessing Directives](../vs140/Preprocessing-Directives.md)