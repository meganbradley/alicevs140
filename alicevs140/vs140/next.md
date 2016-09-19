---
title: "next"
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
ms.assetid: c0dbc96c-38cf-4f67-9fe8-e0967e054329
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# next
Iterates a specified number of times and returns the new iterator position.  
  
## Syntax  
  
```  
template<class InputIterator>  
  InputIterator next(  
    InputIterator _First,  
    typename iterator_traits<InputIterator>::difference_type _Off = 1   
  );  
```  
  
#### Parameters  
 `_First`  
 The current position.  
  
 `_Off`  
 The number of times to iterate.  
  
## Return Value  
 Returns the new iterator position after iterating `_Off` times.  
  
## Remarks  
 The template function returns `next` incremented `_Off` times  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [<iterator\>](../vs140/-iterator-.md)   
 [advance](../vs140/advance--STL-Samples-.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)