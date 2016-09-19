---
title: "unordered_multiset::emplace_hint"
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
ms.assetid: 71c1a5b6-a07d-48df-83da-37937e6df1d8
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unordered_multiset::emplace_hint
Inserts an element constructed in place (no copy or move operations are performed), with a placement hint.  
  
## Syntax  
  
```  
template<class... Args>  
   iterator emplace_hint(  
      const_iterator where,  
      Args&&... args);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|`args`|The arguments forwarded to construct an element to be inserted into the unordered_multiset.|  
|`where`|A hint regarding the place to start searching for the correct point of insertion.|  
  
## Return Value  
 An iterator to the newly inserted element.  
  
## Remarks  
 No references to container elements are invalidated by this function, but it may invalidate all iterators to the container.  
  
 During the insertion, if an exception is thrown but does not occur in the container's hash function, the container is not modified. If the exception is thrown in the hash function, the result is undefined.  
  
 For a code example, see [set::emplace_hint](../vs140/set--emplace_hint.md).  
  
## Requirements  
 **Header:** <unordered_set>  
  
 **Namespace:** std  
  
## See Also  
 [<unordered_set>](../vs140/-unordered_set-.md)   
 [unordered_multiset Class](../vs140/unordered_multiset-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)