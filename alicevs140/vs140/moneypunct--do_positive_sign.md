---
title: "moneypunct::do_positive_sign"
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
ms.assetid: 6c539157-a2dc-4802-b5d1-87a7746ce27c
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# moneypunct::do_positive_sign
A protected virtual member function that returns a locale-specific sequence of elements to use as a positive sign.  
  
## Syntax  
  
```  
virtual string_type do_positive_sign( ) const;  
```  
  
## Return Value  
 A locale-specific sequence of elements to use as a positive sign.  
  
## Example  
 See the example for [positive_sign](../vs140/moneypunct--positive_sign.md), where the virtual member function is called by `positive_sign`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [moneypunct Class](../vs140/moneypunct-Class.md)