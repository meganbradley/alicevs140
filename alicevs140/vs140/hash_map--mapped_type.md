---
title: "hash_map::mapped_type"
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
ms.assetid: 32721312-3d55-4a9c-92ec-5fdeaf7ec972
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_map::mapped_type
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_map Class](../vs140/unordered_map-Class.md).  
  
 A type that represents the data type stored in a hash_map.  
  
## Syntax  
  
```  
typedef Type mapped_type;  
```  
  
## Remarks  
 The type `mapped_type` is a synonym for the template parameter `Type`.  
  
 For more information on `Type` see the [hash_map Class](../vs140/hash_map-Class.md) topic.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
 See example for [value_type](../vs140/hash_map--value_type.md) for an example of how to declare and use `key_type`.  
  
## Requirements  
 **Header:** <hash_map>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_map Class](../vs140/hash_map-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)