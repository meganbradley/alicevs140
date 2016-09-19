---
title: "CControlBar::CalcFixedLayout"
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
ms.assetid: a13e9c7f-4a17-40d1-abc9-fff7cbda5a97
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CControlBar::CalcFixedLayout
Call this member function to calculate the horizontal size of a control bar.  
  
## Syntax  
  
```  
  
      virtual CSize CalcFixedLayout(  
   BOOL bStretch,  
   BOOL bHorz   
);  
```  
  
#### Parameters  
 `bStretch`  
 Indicates whether the bar should be stretched to the size of the frame. The `bStretch` parameter is nonzero when the bar is not a docking bar (not available for docking) and is 0 when it is docked or floating (available for docking).  
  
 `bHorz`  
 Indicates that the bar is horizontally or vertically oriented. The `bHorz` parameter is nonzero if the bar is horizontally oriented and is 0 if it is vertically oriented.  
  
## Return Value  
 The control bar size, in pixels, of a `CSize` object.  
  
## Remarks  
 Control bars such as toolbars can stretch horizontally or vertically to accommodate the buttons contained in the control bar.  
  
 If `bStretch` is **TRUE**, stretch the dimension along the orientation provided by `bHorz`. In other words, if `bHorz` is **FALSE**, the control bar is stretched vertically. If `bStretch` is **FALSE**, no stretch occurs. The following table shows the possible permutations, and resulting control-bar styles, of `bStretch` and `bHorz`.  
  
|bStretch|bHorz|Stretching|Orientation|Docking/Not docking|  
|--------------|-----------|----------------|-----------------|--------------------------|  
|**TRUE**|**TRUE**|Horizontal stretching|Horizontally oriented|Not docking|  
|**TRUE**|**FALSE**|Vertical stretching|Vertically oriented|Not docking|  
|**FALSE**|**TRUE**|No stretching available|Horizontally oriented|Docking|  
|**FALSE**|**FALSE**|No stretching available|Vertically oriented|Docking|  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CControlBar Class](../vs140/CControlBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CControlBar::CalcDynamicLayout](../vs140/CControlBar--CalcDynamicLayout.md)