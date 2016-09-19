---
title: "codecvt::do_max_length"
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
ms.assetid: 20cdb85a-7ec1-4690-b73f-ef7028b373e9
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# codecvt::do_max_length
A virtual function that returns the maximum number of external **Byte**s necessary to produce one internal **CharType**.  
  
## Syntax  
  
```  
virtual int do_max_length( ) const throw( );  
```  
  
## Return Value  
 The maximum number of **Byte**s necessary to produce one **CharType**.  
  
## Remarks  
 The protected virtual member function returns the largest permissible value that can be returned by [do_length](../vs140/codecvt--do_length.md)(`_First1`, `_Last1`, 1) for arbitrary valid values of `_First1` and `_Last1`.  
  
## Example  
 See the example for [max_length](../vs140/codecvt--max_length.md), which calls `do_max_length`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [codecvt Class](../vs140/codecvt-Class.md)