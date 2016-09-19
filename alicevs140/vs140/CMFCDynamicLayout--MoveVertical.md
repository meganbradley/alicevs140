---
title: "CMFCDynamicLayout::MoveVertical"
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
ms.assetid: 60aeeb8a-98fc-42f7-8c1a-8d1f7cec141d
caps.latest.revision: 6
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDynamicLayout::MoveVertical
Gets a [MoveSettings](../vs140/CMFCDynamicLayout--MoveSettings-Structure.md) value that defines how much a child control is moved vertically when the user resizes its hosting window.  
  
## Syntax  
  
```vb  
  
static MoveSettings MoveVertical(    int nRatio);  
```  
  
#### Parameters  
 `nRatio`  
 Defines as a percentage how far a child control is moved vertically when the user resizes the host window.  
  
## Return Value  
 A [MoveSettings](../vs140/CMFCDynamicLayout--MoveSettings-Structure.md) value that encapsulates the requested move ratio.  
  
## Remarks  
  
## Requirements  
 **Header:** afxlayout.h  
  
## See Also  
 [CMFCDynamicLayout Class](../vs140/CMFCDynamicLayout-Class.md)   
 [CMFCDynamicLayout::MoveSettings Structure](../vs140/CMFCDynamicLayout--MoveSettings-Structure.md)