---
title: "moneypunct::do_decimal_point"
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
ms.assetid: 800fe536-df63-4b1b-88b2-b96351e7f51e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# moneypunct::do_decimal_point
A protected virtual member function that returns a locale-specific sequence of elements to use as a decimal point symbol.  
  
## Syntax  
  
```  
virtual CharType do_decimal_point( ) const;  
```  
  
## Return Value  
 A locale-specific sequence of elements to use as a decimal point symbol.  
  
## Example  
 See the example for [decimal_point](../vs140/moneypunct--decimal_point.md), where the virtual member function is called by `decimal_point`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [moneypunct Class](../vs140/moneypunct-Class.md)