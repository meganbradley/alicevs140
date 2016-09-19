---
title: "hash_map::const_iterator"
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
ms.assetid: 6f00da85-ad2c-4e0c-bdb5-205d319889d1
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_map::const_iterator
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_map Class](../vs140/unordered_map-Class.md).  
  
 A type that provides a bidirectional iterator that can read a **const** element in the hash_map.  
  
## Syntax  
  
```  
typedef list<typename Traits::value_type, typename Traits::allocator_type>::const_iterator const_iterator;  
```  
  
## Remarks  
 A type `const_iterator` cannot be used to modify the value of an element.  
  
 The `const_iterator` defined by hash_map points to elements that are objects of [value_type](../vs140/hash_map--value_type.md), that is of type `pair`*<***const Key, Type***>*, whose first member is the key to the element and whose second member is the mapped datum held by the element.  
  
 To dereference a `const_iterator` `cIter` pointing to an element in a hash_map, use the **->** operator.  
  
 To access the value of the key for the element, use `cIter` **-> first**, which is equivalent to (\*`cIter`)**.first**. To access the value of the mapped datum for the element, use `cIter` **-> second**, which is equivalent to (\*`cIter`)**.second**.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
 See example for [begin](../vs140/hash_map--begin.md) for an example using `const_iterator`.  
  
## Requirements  
 **Header:** <hash_map>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_map Class](../vs140/hash_map-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)