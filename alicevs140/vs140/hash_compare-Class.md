---
title: "hash_compare Class"
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
ms.assetid: d502bb59-de57-4585-beb9-00e3a998c0af
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_compare Class
The template class describes an object that can be used by any of the hash associative containers — hash_map, hash_multimap, hash_set, or hash_multiset — as a default **Traits** parameter object to order and hash the elements they contain.  
  
## Syntax  
  
```  
template<class Key, class Traits = less<Key> >  
   class hash_compare  
   {  
   Traits comp;  
public:  
   const size_t bucket_size = 4;  
   const size_t min_buckets = 8;  
   hash_compare( );  
   hash_compare( Traits pred );  
   size_t operator( )( const Key& _Key ) const;  
   bool operator( )(   
      const Key& _Key1,  
      const Key& _Key2  
   ) const;  
   };  
```  
  
## Remarks  
 Each hash associative container stores a hash traits object of type **Traits** (a template parameter). You can derive a class from a specialization of hash_compare to selectively override certain functions and objects, or you can supply your own version of this class if you meet certain minimum requirements. Specifically, for an object hash_comp of type **hash_compare<Key, Traits>**, the following behavior is required by the above containers:  
  
-   For all values `_Key` of type **Key**, the call **hash_comp**( `_Key`) serves as a hash function, which yields a distribution of values of type **size_t**. The function supplied by hash_compare returns `_Key`.  
  
-   For any value `_Key1` of type **Key** that precedes `_Key2` in the sequence and has the same hash value (value returned by the hash function), **hash_comp**( `_Key2`, `_Key1`) is false. The function must impose a total ordering on values of type **Key**. The function supplied by hash_compare returns                         *comp*( `_Key2`, `_Key1`) `,` where                         *comp* is a stored object of type **Traits** that you can specify when you construct the object hash_comp. For the default **Traits** parameter type **less<Key\>**, sort keys never decrease in value.  
  
-   The integer constant **bucket_size** specifies the mean number of elements per "bucket" (hash-table entry) that the container should try not to exceed. It must be greater than zero. The value supplied by hash_compare is 4.  
  
-   The integer constant **min_buckets** specifies the minimum number of buckets to maintain in the hash table. It must be a power of two and greater than zero. The value supplied by hash_compare is 8.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
 See examples for [hash_map::hash_map](../vs140/hash_map-Class.md#hash_map__hash_map), [hash_multimap::hash_multimap](../vs140/hash_multimap-Class.md#hash_multimap__hash_multimap), [hash_set::hash_set](../vs140/hash_set-Class.md#hash_set__hash_set), and [hash_multiset::hash_multiset](../vs140/hash_multiset-Class.md#hash_multiset__hash_multiset), for examples of how to declare and use hash_compare.  
  
## Requirements  
 **Header:** <hash_map>  
  
 **Namespace:** stdext  
  
## See Also  
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)