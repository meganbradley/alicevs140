---
title: "hash_set::insert"
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
ms.assetid: 80dcbb50-31c6-4f23-8b45-b195318f1f15
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_set::insert
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_set Class](../vs140/unordered_set-Class.md).  
  
 Inserts an element or a range of elements into a `hash_set`.  
  
## Syntax  
  
```  
pair<iterator, bool> insert(  
   const value_type& Val  
);  
iterator insert(  
   iterator Where,  
   const value_type& Val  
); void insert(  
    initializer_list<value_type> IList  
)  
template<class InputIterator>  
   void insert(  
      InputIterator First,  
      InputIterator Last  
);  
  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|`Val`|The value of an element to be inserted into the `hash_set` unless the `hash_set` already contains that element or, more generally, an element whose key is equivalently ordered.|  
|`Where`|The place to start searching for the correct point of insertion. (Insertion can occur in amortized constant time, instead of logarithmic time, if the insertion point immediately follows `_Where`.)|  
|`First`|The position of the first element to be copied from a `hash_set`.|  
|`Last`|The position just beyond the last element to be copied from a `hash_set`.|  
|`IList`|The initializer_list from which to copy the elements.|  
  
## Return Value  
 The first `insert` member function returns a pair whose `bool` component returns `true` if an insertion was make and `false` if the `hash_set` already contained an element whose key had an equivalent value in the ordering, and whose iterator component returns the address where a new element was inserted or where the element was already located.  
  
 To access the iterator component of a pair `pr` returned by this member function, use `pr.first` and to dereference it, use `*(pr.first)`. To access the `bool` component of a pair `pr` returned by this member function, use `pr.second`, and to dereference it, use `*(pr.second)`.  
  
 The second `insert` member function returns an iterator that points to the position where the new element was inserted into the `hash_set`.  
  
## Remarks  
 The third member function inserts the elements in an initializer_list.  
  
 The third member function inserts the sequence of element values into a `hash_set` corresponding to each element addressed by an iterator of in the range [`First`, `Last`) of a specified `hash_set`.  
  
## Requirements  
 **Header:** <hash_set>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_set Class](../vs140/hash_set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)