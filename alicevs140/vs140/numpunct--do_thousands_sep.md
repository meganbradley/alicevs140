---
title: "numpunct::do_thousands_sep"
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
ms.assetid: d0ef49e9-c0f3-41e9-8159-8e3d62a1ff84
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# numpunct::do_thousands_sep
A protected virtual member function that is called to return a locale-specific element to use as a thousands separator.  
  
## Syntax  
  
```  
virtual CharType do_thousands_sep( ) const;  
```  
  
## Return Value  
 Returns a locale-specific element to use as a thousands separator.  
  
## Remarks  
 The protected virtual member function returns a locale-specific element of type **CharType** to use as a group separator to the left of any decimal point.  
  
## Example  
 See the example for [thousands_sep](../vs140/numpunct--thousands_sep.md), where the virtual member function is called by `thousands_sep`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [numpunct Class](../vs140/numpunct-Class.md)