---
title: "forward_list::clear"
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
ms.assetid: 3ecf7923-8500-4c20-8108-cf7d8efb5e6b
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# forward_list::clear
Erases all the elements of a forward list.  
  
## Syntax  
  
```  
void clear();  
```  
  
## Remarks  
 This member function calls `erase_after(before_begin(), end()).`  
  
## Requirements  
 **Header:** <forward_list>  
  
 **Namespace:** std  
  
## See Also  
 [forward_list Class](../vs140/forward_list-Class.md)