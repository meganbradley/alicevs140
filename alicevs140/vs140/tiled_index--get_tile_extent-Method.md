---
title: "tiled_index::get_tile_extent Method"
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
ms.assetid: 978ed5bd-51ef-49e4-b88f-794ea694dad2
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# tiled_index::get_tile_extent Method
Returns an [extent](../vs140/extent-Class--C---AMP-.md) object that has the values of the [tiled_index](../vs140/tiled_index-Class.md) template arguments `_Dim0`, `_Dim1`, and `_Dim2`.  
  
## Syntax  
  
```  
extent<rank> get_tile_extent()restrict(amp,cpu);  
```  
  
## Return Value  
 An `extent` object that has the values of the `tiled_index` template arguments `_Dim0`, `_Dim1`, and `_Dim2`.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [tiled_index Class](../vs140/tiled_index-Class.md)