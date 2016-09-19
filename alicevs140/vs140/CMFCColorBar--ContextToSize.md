---
title: "CMFCColorBar::ContextToSize"
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
ms.assetid: 871de66c-18c3-4860-9a15-50728ac4ab8c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorBar::ContextToSize
Calculates the vertical and horizontal margins that are required to contain the buttons on the color bar control, and adjusts the location of those buttons.  
  
## Syntax  
  
```  
void ContextToSize(  
   BOOL bSquareButtons = TRUE,   
   BOOL bCenterButtons = TRUE  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `bSquareButtons`|`TRUE` to specify that the shape of the buttons on a color bar control are square; otherwise, `FALSE`. The default value is `TRUE`.|  
|[in] `bCenterButtons`|`TRUE` to specify that the content on the face of a color bar control button is centered; otherwise, `FALSE`. The default value is `TRUE`.|  
  
## Remarks  
  
## Requirements  
 **Header:** afxcolorbar.h  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)   
 [CMFCColorBar::AdjustLocations](../vs140/CMFCColorBar--AdjustLocations.md)