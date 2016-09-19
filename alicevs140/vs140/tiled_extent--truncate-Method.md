---
title: "tiled_extent::truncate Method"
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
ms.assetid: 9ca7ae6a-e0ed-483b-b890-070d4ccd73eb
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# tiled_extent::truncate Method
Returns a new `tiled_extent` object with extents adjusted down to be evenly divisible by the tile dimensions.  
  
## Syntax  
  
```  
tiled_extent truncate() const;  
```  
  
## Return Value  
 Returns a new `tiled_extent` object with extents adjusted down to be evenly divisible by the tile dimensions.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [tiled_extent Class](../vs140/tiled_extent-Class.md)