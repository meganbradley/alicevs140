---
title: "moneypunct::do_curr_symbol"
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
ms.assetid: a652639d-108f-4820-b674-0a5e8227f0d3
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# moneypunct::do_curr_symbol
A protected virtual member function that returns a locale-specific sequence of elements to use as a currency symbol.  
  
## Syntax  
  
```  
virtual string_type do_curr_symbol( ) const;  
```  
  
## Return Value  
 A locale-specific sequence of elements to use as a decimal point symbol.  
  
## Example  
 See the example for [curr_symbol](../vs140/moneypunct--curr_symbol.md), where the virtual member function is called by `curr_symbol`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [moneypunct Class](../vs140/moneypunct-Class.md)