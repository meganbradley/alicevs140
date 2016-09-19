---
title: "CDC::GetHalftoneBrush"
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
ms.topic: reference
ms.assetid: 8592d5f3-dc4a-486c-aa0c-2f6014e4ce3f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetHalftoneBrush
Call this member function to retrieve a halftone brush.  
  
## Syntax  
  
```  
  
static CBrush* PASCAL GetHalftoneBrush( );  
  
```  
  
## Return Value  
 A pointer to a `CBrush` object if successful; otherwise **NULL**.  
  
## Remarks  
 A halftone brush shows pixels that are alternately foreground and background colors to create a dithered pattern. The following is an example of a dithered pattern created by a halftone brush.  
  
 ![Detail of a dithered pen stroke](../vs140/media/vc318S1.gif "vc318S1")  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBrush Class](../vs140/CBrush-Class.md)