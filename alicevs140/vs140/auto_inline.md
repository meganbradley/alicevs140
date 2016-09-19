---
title: "auto_inline"
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
ms.assetid: f7624cd1-be76-429a-881c-65c9040acf43
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# auto_inline
Excludes any functions defined within the range where **off** is specified from being considered as candidates for automatic inline expansion.  
  
## Syntax  
  
```  
  
#pragma auto_inline( [{on | off}] )  
```  
  
## Remarks  
 To use the **auto_inline** pragma, place it before and immediately after (not in) a function definition. The pragma takes effect at the first function definition after the pragma is seen.  
  
## See Also  
 [Pragma Directives and the __Pragma Keyword](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md)