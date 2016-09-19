---
title: "all_of"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 11770601-c597-4b1a-9796-88490853c385
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# all_of
Returns `true` when a condition is present at each element in the given range.  
  
## Syntax  
  
```  
template<class InputIterator, class Predicate>  
    bool all_of(  
        InputIterator _First,   
        InputIterator _Last,   
        BinaryPredicate _Comp  
    );  
```  
  
#### Parameters  
 `_First`  
 An input iterator that indicates where to start to check for a condition. The iterator marks where a range of elements starts.  
  
 `_Last`  
 An input iterator that indicates the end of the range of elements to check for a condition.  
  
 `_Comp`  
 A condition to test for. This is a user-defined predicate function object that defines the condition to be satisfied by an element being checked. A predicate takes a single argument and returns `true` or `false`.  
  
## Return Value  
 Returns `true` if the condition is detected at each element in the indicated range, and `false` if the condition is not detected at least one time.  
  
## Remarks  
 The template function returns `true` only if, for each `N` in the range `[0, _Last - _First)`, the predicate `_Comp(*(_First + N))` is `true`.  
  
## Requirements  
 **Header:** <algorithm\>  
  
 **Namespace:** std  
  
## See Also  
 [any_of](../vs140/any_of.md)   
 [none_of](../vs140/none_of.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)