---
title: "alignment_of Class"
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
ms.assetid: 4141c59a-f94e-41c4-93fd-9ea578b27387
caps.latest.revision: 22
translation.priority.mt: 
  - de-de
  - ja-jp
---
# alignment_of Class
Gets alignment of the specified type. This struct is implemented in terms of [alignof](../vs140/alignof-and-alignas--C---.md). Use `alignof` directly when you simply need to query an alignment value. Use alignment_of when you need an integral constant, for example when doing tag dispatch.  
  
## Syntax  
  
```  
template<class Ty>  
    struct alignment_of;  
```  
  
#### Parameters  
 `Ty`  
 The type to query.  
  
## Remarks  
 The type query holds the value of the the alignment of the type `Ty`.  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [aligned_storage](../vs140/aligned_storage-Class.md)