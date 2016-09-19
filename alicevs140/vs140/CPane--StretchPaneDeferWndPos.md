---
title: "CPane::StretchPaneDeferWndPos"
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
ms.assetid: 8efaeb94-d30b-4174-8703-22bc5f44fa8b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::StretchPaneDeferWndPos
Stretches the pane vertically or horizontally based on docking style.  
  
## Syntax  
  
```  
virtual int StretchPaneDeferWndPos(  
   int nStretchSize,  
   HDWP& hdwp  
);  
```  
  
#### Parameters  
 [in] `nStretchSize`  
 The amount, in pixels, to stretch the pane. Use a negative value to shrink the pane.  
  
 [in] `hdwp`  
 Not used.  
  
## Return Value  
 The actual amount, in pixels, that the pane was stretched.  
  
## Remarks  
 If necessary, this method modifies `nStretchSize` to ensure that the pane does not exceed size limits. These limits are obtained by calling [CPane::GetAvailableStretchSize](../vs140/CPane--GetAvailableStretchSize.md) and [CPane::GetAvailableExpandSize](../vs140/CPane--GetAvailableExpandSize.md).  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)