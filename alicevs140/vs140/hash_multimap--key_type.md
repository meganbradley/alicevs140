---
title: "hash_multimap::key_type"
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
ms.assetid: b0ab4acf-0688-4094-be9f-10645afcce2d
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_multimap::key_type
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_multimap Class](../vs140/unordered_multimap-Class.md).  
  
 A type that describes the sort key object that constitutes each element of the hash_multimap.  
  
## Syntax  
  
```  
typedef Key key_type;  
```  
  
## Remarks  
 `key_type` is a synonym for the template parameter `Key`.  
  
 For more information on `Key`, see the Remarks section of the [hash_multimap Class](../vs140/hash_multimap-Class.md) topic.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
 See the example for [value_type](../vs140/hash_multimap--value_type.md) for an example of how to declare and use `key_compare`.  
  
## Requirements  
 **Header:** <hash_map>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_multimap Class](../vs140/hash_multimap-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)