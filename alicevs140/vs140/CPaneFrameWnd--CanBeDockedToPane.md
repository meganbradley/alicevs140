---
title: "CPaneFrameWnd::CanBeDockedToPane"
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
ms.assetid: 61dcb452-971c-44a1-898c-7a995f3b09d7
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::CanBeDockedToPane
Determines whether the mini-frame window can be docked to a pane.  
  
## Syntax  
  
```  
virtual BOOL CanBeDockedToPane(  
   const CDockablePane* pDockingBar  
) const;  
```  
  
#### Parameters  
 [in] `pDockingBar`  
 A pane.  
  
## Return Value  
 Nonzero if the mini-frame can be docked to `pDockingBar`; otherwise 0.  
  
## Requirements  
 **Header:** afxpaneframewnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)