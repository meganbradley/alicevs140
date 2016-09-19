---
title: "CMFCColorBar::AllowChangeTextLabels"
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
ms.assetid: 3f91dd61-4cd2-4cf5-a7fd-1748a618497d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorBar::AllowChangeTextLabels
Indicates whether the text label of color buttons can change.  
  
## Syntax  
  
```  
virtual BOOL AllowChangeTextLabels() const;  
```  
  
## Return Value  
 Always `FALSE`.  
  
## Remarks  
 By default, this method always returns `FALSE`, which means text labels cannot be modified. Override this method to enable modifying text labels.  
  
## Requirements  
 **Header:** afxcolorbar.h  
  
## See Also  
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)