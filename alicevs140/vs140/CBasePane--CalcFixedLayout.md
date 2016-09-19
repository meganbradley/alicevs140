---
title: "CBasePane::CalcFixedLayout"
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
ms.assetid: 41666d79-3a1c-48de-bf37-8fbdede599e4
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::CalcFixedLayout
Calculates the horizontal size of a control bar.  
  
## Syntax  
  
```  
virtual CSize CalcFixedLayout(  
   BOOL bStretch,  
   BOOL bHorz  
);  
```  
  
#### Parameters  
 [in] `bStretch`  
 Indicates whether the bar should be stretched to the size of the frame. The `bStretch` parameter is nonzero when the bar is not a docking bar (not available for docking) and is 0 when it is docked or floating (available for docking).  
  
 [in] `bHorz`  
 Indicates that the bar is horizontally or vertically oriented. The `bHorz` parameter is nonzero if the bar is horizontally oriented and is 0 if it is vertically oriented.  
  
## Return Value  
 The control bar size, in pixels, of a `CSize` object.  
  
## Remarks  
 See the remarks section in [CControlBar::CalcFixedLayout](../vs140/CControlBar--CalcFixedLayout.md)  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)