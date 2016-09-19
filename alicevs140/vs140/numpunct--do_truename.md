---
title: "numpunct::do_truename"
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
ms.assetid: 5da6e2a3-34f0-4601-b8b7-9da09c8dfe70
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# numpunct::do_truename
A protected virtual member function that is called to return a string to use as a text representation of the value **true**.  
  
## Syntax  
  
```  
virtual string_type do_truename( ) const;  
```  
  
## Remarks  
 A string to use as a text representation of the value **true**.  
  
 All locales return a string "true" to represent the value **true**.  
  
## Example  
 See the example for [truename](../vs140/numpunct--truename.md), where the virtual member function is called by `truename`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [numpunct Class](../vs140/numpunct-Class.md)