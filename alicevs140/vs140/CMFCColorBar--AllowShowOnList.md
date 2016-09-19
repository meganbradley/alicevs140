---
title: "CMFCColorBar::AllowShowOnList"
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
ms.assetid: 2d382cd7-f6f8-4fb5-9091-aadf0fd20f51
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorBar::AllowShowOnList
Indicates whether the color bar control object can appear in a toolbar list during the customization process.  
  
## Syntax  
  
```  
virtual BOOL AllowShowOnList() const;  
```  
  
## Return Value  
 Always `TRUE`.  
  
## Remarks  
 By default, this method always returns `TRUE`, which means the framework can display the color bar control during the customization process. Override this method to implement a different behavior.  
  
## Requirements  
 **Header:** afxcolorbar.h  
  
## See Also  
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)