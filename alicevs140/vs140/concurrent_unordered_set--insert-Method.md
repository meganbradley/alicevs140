---
title: "concurrent_unordered_set::insert Method"
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
ms.assetid: 60fe2015-234b-4d70-bb79-e232b14ea330
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_set::insert Method
Adds elements to the `concurrent_unordered_set` object.  
  
## Syntax  
  
```  
std::pair<iterator, bool> insert(  
   const value_type& _Value  
);  
  
iterator insert(  
   const_iterator _Where,  
   const value_type& _Value  
);  
  
template<  
   class _Iterator  
>  
void insert(  
   _Iterator_First,  
   _Iterator_Last  
);  
  
template<  
   class _Valty  
>  
std::pair<iterator, bool> insert(  
   _Valty&& _Value  
);  
  
template<  
   class _Valty  
>  
typename std::tr1::enable_if<!std::tr1::is_same<const_iterator, typename std::tr1::remove_reference<_Valty>::type>::value, iterator>::type insert(  
   const_iterator _Where,  
   _Valty&& _Value  
);  
```  
  
#### Parameters  
 `_Iterator`  
 The iterator type used for insertion.  
  
 `_Valty`  
 The type of the value inserted into the set.  
  
 `_Value`  
 The value to be inserted.  
  
 `_Where`  
 The starting location to search for an insertion point.  
  
 `_First`  
 The beginning of the range to insert.  
  
 `_Last`  
 The end of the range to insert.  
  
## Return Value  
 A pair that contains an iterator and a boolean value. See the Remarks section for more details.  
  
## Remarks  
 The first member function determines whether an element X exists in the sequence whose key has equivalent ordering to that of `_Value`. If not, it creates such an element X and initializes it with `_Value`. The function then determines the iterator `where` that designates X. If an insertion occurred, the function returns `std::pair(where, true)`. Otherwise, it returns `std::pair(where, false)`.  
  
 The second member function returns insert(`_Value`), using `_Where` as a starting place within the controlled sequence to search for the insertion point.  
  
 The third member function inserts the sequence of element values from the range [`_First`, `_Last`).  
  
 The last two member functions behave the same as the first two, except that `_Value` is used to construct the inserted value.  
  
## Requirements  
 **Header:** concurrent_unordered_set.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_set Class](../vs140/concurrent_unordered_set-Class.md)