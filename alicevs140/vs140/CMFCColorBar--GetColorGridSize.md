---
title: "CMFCColorBar::GetColorGridSize"
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
ms.assetid: edd969f1-e8d7-4d26-8775-c6e2a6b6e3a0
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorBar::GetColorGridSize
Calculates the number of rows and columns in the grid of a color bar control.  
  
## Syntax  
  
```  
CSize GetColorGridSize(  
   BOOL bVertDock  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `bVertDock`|`TRUE` to perform the calculation for a vertically docked color bar control; otherwise, perform the calculation for a horizontally docked control.|  
  
## Return Value  
 A [CSize](../vs140/CSize-Class.md) object whose `cx` component contains the number of columns and whose `cy` component contains the number of rows.  
  
## Requirements  
 **Header:** afxcolorbar.h  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)