---
title: "tiled_index::operator const index&lt;rank&gt; Operator"
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
ms.assetid: a56cc467-3dd8-4b21-940e-077d7c5e77b7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# tiled_index::operator const index&lt;rank&gt; Operator
Implicitly converts a [tiled_index](../vs140/tiled_index-Class.md) object into an [index](../vs140/index-Class.md) object.  
  
## Syntax  
  
```  
operator const index<rank>() const restrict(cpu, amp)  
  
```  
  
#### Parameters  
 `rank`  
 The rank of the `tiled_index` object.  
  
## Return Value  
 An object of type `index` that contains a copy of the data that is contained in the `tiled_index` object.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [tiled_index Class](../vs140/tiled_index-Class.md)