---
title: "numpunct::do_grouping"
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
ms.assetid: 0e43b8bd-85c0-4179-a38c-6f6cc2822505
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# numpunct::do_grouping
A protected virtual member function that is called to return a locale-specific rule for determining how digits are grouped to the left of any decimal point.  
  
## Syntax  
  
```  
virtual string do_grouping( ) const;  
```  
  
## Return Value  
 A locale-specific rule for determining how digits are grouped to the left of any decimal point.  
  
## Remarks  
 The protected virtual member function returns a locale-specific rule for determining how digits are grouped to the left of any decimal point. The encoding is the same as for **lconv::grouping**.  
  
## Example  
 See the example for [grouping](../vs140/numpunct--grouping.md), where the virtual member function is called by **grouping**.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [numpunct Class](../vs140/numpunct-Class.md)