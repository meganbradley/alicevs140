---
title: "CPane::MovePane"
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
ms.assetid: f84ee750-9502-4255-ae95-22032f6d51c6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::MovePane
Moves the pane to the specified rectangle.  
  
## Syntax  
  
```  
virtual CSize MovePane(  
   CRect rectNew,  
   BOOL bForceMove,  
   HDWP& hdwp  
);  
```  
  
#### Parameters  
 [in] `rectNew`  
 Specifies the new rectangle for the pane.  
  
 [in] `bForceMove`  
 If `TRUE`, this method ignores the minimum allowed pane size ([CPane::GetMinSize](../vs140/CPane--GetMinSize.md)); otherwise, the pane is adjusted, if necessary, to ensure that it is at least the minimum allowed size.  
  
 [in] `hdwp`  
 Not used.  
  
## Return Value  
 A `CSize` object that contains the differences in width and height between the new and old rectangles (old rectangle –`rectNew`).  
  
## Remarks  
 This method is used only for dockable panes.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart)](../vs140/Hierarchy-Chart.md)