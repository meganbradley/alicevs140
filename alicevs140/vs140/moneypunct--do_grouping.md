---
title: "moneypunct::do_grouping"
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
ms.assetid: 6f9c1078-185c-4f3f-836b-c529c04f39d3
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# moneypunct::do_grouping
A protected virtual member function that returns a locale-specific rule for determining how digits are grouped to the left of any decimal point.  
  
## Syntax  
  
```  
virtual string do_grouping( ) const;  
```  
  
## Return Value  
 A locale-specific rule for determining how digits are grouped to the left of any decimal point.  
  
## Example  
 See the example for [grouping](../vs140/moneypunct--grouping.md), where the virtual member function is called by **grouping**.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [moneypunct Class](../vs140/moneypunct-Class.md)