---
title: "swap (hash_set)"
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
ms.assetid: 303b6244-5a97-49a2-a81f-2a4edc0852eb
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# swap (hash_set)
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_set Class](../vs140/unordered_set-Class.md).  
  
 Exchanges the elements of two hash_sets.  
  
## Syntax  
  
```  
void swap(  
   hash_set <Key, Traits, Allocator>& _Left,  
   hash_set <Key, Traits, Allocator>& _Right  
);  
```  
  
#### Parameters  
 `_Right`  
 The hash_set providing the elements to be swapped, or the hash_set whose elements are to be exchanged with those of the hash_set `_Left`.  
  
 `_Left`  
 The hash_set whose elements are to be exchanged with those of the hash_set `_Right`.  
  
## Remarks  
 The `swap` template function is an algorithm specialized on the container class hash_set to execute the member function `_Left``.`[swap](../vs140/hash_set--swap.md)(`_Right`). This is an instance of the partial ordering of function templates by the compiler. When template functions are overloaded in such a way that the match of the template with the function call is not unique, then the compiler will select the most specialized version of the template function. The general version of the template function  
  
 **template <class T\> void swap(T&, T&),**  
  
 in the algorithm class works by assignment and is a slow operation. The specialized version in each container is much faster as it can work with the internal representation of the container class.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
 See the code example for the member class [hash_set::swap](../vs140/hash_set--swap.md) for an example that uses the template version of `swap`.  
  
## Requirements  
 **Header:** <hash_set>  
  
 **Namespace:** stdext  
  
## See Also  
 [Standard Template Library](../vs140/Standard-Template-Library.md)