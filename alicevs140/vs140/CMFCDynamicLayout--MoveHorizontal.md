---
title: "CMFCDynamicLayout::MoveHorizontal"
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
ms.assetid: d32eaa29-2490-47a3-9125-35e2338d83c6
caps.latest.revision: 6
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDynamicLayout::MoveHorizontal
Gets a [MoveSettings](../vs140/CMFCDynamicLayout--MoveSettings-Structure.md) value that defines how much a child control is moved horizontally when the user resizes its hosting window.  
  
## Syntax  
  
```vb  
  
static MoveSettings MoveHorizontal(    int nRatio);  
```  
  
#### Parameters  
 `nRatio`  
 Defines as a percentage how far a child control is moved horizontally when the user resizes the host window.  
  
## Return Value  
 A [MoveSettings](../vs140/CMFCDynamicLayout--MoveSettings-Structure.md) value that encapsulates the requested move ratio.  
  
## Remarks  
  
## Requirements  
 **Header:** afxlayout.h  
  
## See Also  
 [CMFCDynamicLayout Class](../vs140/CMFCDynamicLayout-Class.md)   
 [CMFCDynamicLayout::MoveSettings Structure](../vs140/CMFCDynamicLayout--MoveSettings-Structure.md)