---
title: "hash_multimap::key_compare"
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
ms.assetid: 1e2e6c68-979d-40af-8fda-47a6aadede29
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_multimap::key_compare
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_multimap Class](../vs140/unordered_multimap-Class.md).  
  
 A type that provides a function object that can compare two sort keys to determine the relative order of two elements in the hash_multimap.  
  
## Syntax  
  
```  
typedef Traits key_compare;  
```  
  
## Remarks  
 **key_compare** is a synonym for the template parameter `Traits`.  
  
 For more information on `Traits` see the [hash_multimap Class](../vs140/hash_multimap-Class.md) topic.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
 See the example for [key_comp](../vs140/hash_multimap--key_comp.md) for an example of how to declare and use `key_compare`.  
  
## Requirements  
 **Header:** <hash_map>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_multimap Class](../vs140/hash_multimap-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)