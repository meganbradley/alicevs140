---
title: "hash_multiset::insert"
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
ms.assetid: 44cea9f3-8077-4fb2-9956-f3e732fc02ad
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_multiset::insert
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_multiset Class](../vs140/unordered_multiset-Class.md).  
  
 Inserts an element or a range of elements into a hash_multiset.  
  
## Syntax  
  
```  
iterator insert(  
    const Type& Val  
);  
iterator insert(  
    iterator Where,  
    const Type& Al  
);  
void insert(  
     initializer_list<Type> IList  
);  
iterator insert(  
    const Type& Val  
);  
iterator insert(  
    Iterator Where,   
    const Type& Val  
);  
template<class InputIterator>  
    void insert(  
        InputIterator First,  
        InputIterator Last  
    );  
template<class ValTy>  
     iterator insert(  
          ValTy&& Val  
);  
template<class ValTy>  
     iterator insert(  
          const_iterator Where,  
          ValTy&& Val  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|`Val`|The value of an element to be inserted into the hash_multiset unless the hash_multiset already contains that element or, more generally, an element whose key is equivalently ordered.|  
|`Where`|The place to start searching for the correct point of insertion. (Insertion can occur in amortized constant time, instead of logarithmic time, if the insertion point immediately follows `_Where`.)|  
|`First`|The position of the first element to be copied from a hash_multiset.|  
|`Last`|The position just beyond the last element to be copied from a hash_multiset.|  
|`IList`|The initializer_list that contains the elements to copy.|  
  
## Return Value  
 The first two insert member functions return an iterator that points to the position where the new element was inserted.  
  
 The next three member functions use an initializer_list.  
  
 The third member function inserts the sequence of element values into a hash_multiset corresponding to each element addressed by an iterator of in the range [`First`, `Last`) of a specified hash_multiset.  
  
## Remarks  
 Insertion can occur in amortized constant time for the hint version of insert, instead of logarithmic time, if the insertion point immediately follows `Where`.  
  
## Requirements  
 **Header:** <hash_set>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_multiset Class](../vs140/hash_multiset-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)