---
title: "moneypunct::do_negative_sign"
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
ms.assetid: 3ea91663-f00a-4dc0-8ed7-1ae847eb8c73
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# moneypunct::do_negative_sign
A protected virtual member function that is called to return a locale-specific sequence of elements to use as a negative sign symbol.  
  
## Syntax  
  
```  
virtual string_type do_negative_sign( ) const;  
```  
  
## Return Value  
 A locale-specific sequence of elements to use as a negative sign.  
  
## Example  
 See the example for [negative_sign](../vs140/moneypunct--negative_sign.md), where the virtual member function is called by `negative_sign`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [moneypunct Class](../vs140/moneypunct-Class.md)