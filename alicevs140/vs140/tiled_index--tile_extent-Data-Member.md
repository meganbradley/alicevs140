---
title: "tiled_index::tile_extent Data Member"
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
ms.assetid: e37334a4-0926-4a09-be43-137d8d6ef682
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# tiled_index::tile_extent Data Member
Gets an [extent](../vs140/extent-Class--C---AMP-.md) object that has the values of the [tiled_index](../vs140/tiled_index-Class.md) template arguments [tiled_index](../vs140/tiled_index-Class.md) template arguments `_Dim0`, `_Dim1`, and `_Dim2`.  
  
## Syntax  
  
```  
__declspec(property(get=get_tile_extent)) extent<rank> tile_extent;  
```  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [tiled_index Class](../vs140/tiled_index-Class.md)