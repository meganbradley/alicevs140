---
title: "CMFCColorBar::CalcSize"
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
ms.assetid: 043b3424-a7b7-4505-99b4-27fd86ffc9eb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorBar::CalcSize
Called by the framework as part of the layout calculation process.  
  
## Syntax  
  
```  
virtual CSize CalcSize(  
   BOOL bVertDock   
);  
```  
  
#### Parameters  
 [in] `bVertDock`  
 `TRUE` to specify that the color bar control is docked vertically; `FALSE` to specify that the color bar control is docked horizontally.  
  
## Return Value  
 The size of the array of color buttons in a color bar control.  
  
## Requirements  
 **Header:** afxcolorbar.h  
  
## See Also  
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)