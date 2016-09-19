---
title: "numpunct::do_falsename"
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
ms.assetid: f15b3cfe-31a1-4260-a7e9-c7e48692d6f2
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# numpunct::do_falsename
The protected virtual member function returns a sequence to use as a text representation of the value **false**.  
  
## Syntax  
  
```  
virtual string_type do_falsename( ) const;  
```  
  
## Return Value  
 A string containing a sequence to use as a text representation of the value **false**.  
  
## Remarks  
 The member function returns the string "false" to represent the value **false** in all locales.  
  
## Example  
 See the example for [falsename](../vs140/numpunct--falsename.md), where the virtual member function is called by `falsename`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [numpunct Class](../vs140/numpunct-Class.md)