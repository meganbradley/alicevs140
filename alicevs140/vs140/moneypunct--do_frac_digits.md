---
title: "moneypunct::do_frac_digits"
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
ms.assetid: 513c9238-7acc-44ca-90ec-e26c67b4576d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# moneypunct::do_frac_digits
A protected virtual member function that returns a locale-specific count of the number of digits to display to the right of any decimal point.  
  
## Syntax  
  
```  
virtual int do_frac_digits( ) const;  
```  
  
## Return Value  
 A locale-specific count of the number of digits to display to the right of any decimal point.  
  
## Example  
 See the example for [frac_digits](../vs140/moneypunct--frac_digits.md), where the virtual member function is called by `frac_digits`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [moneypunct Class](../vs140/moneypunct-Class.md)