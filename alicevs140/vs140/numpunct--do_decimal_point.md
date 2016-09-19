---
title: "numpunct::do_decimal_point"
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
ms.assetid: 94eb7497-35b2-4537-aaac-dfa7f5220ad6
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# numpunct::do_decimal_point
A protected virtual member function that is called to return a locale-specific element to use as a decimal point.  
  
## Syntax  
  
```  
virtual CharType do_decimal_point( ) const;  
```  
  
## Return Value  
 A locale-specific element to use as a decimal point.  
  
## Example  
 See the example for [decimal_point](../vs140/numpunct--decimal_point.md), where the virtual member function is called by `decimal_point`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [numpunct Class](../vs140/numpunct-Class.md)