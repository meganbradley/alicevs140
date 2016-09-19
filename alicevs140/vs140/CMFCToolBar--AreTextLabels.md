---
title: "CMFCToolBar::AreTextLabels"
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
ms.assetid: 926d2307-902a-48ea-82eb-0cb0dfce0c65
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::AreTextLabels
Specifies whether text labels under images are currently displayed on the toolbar buttons.  
  
## Syntax  
  
```  
BOOL AreTextLabels() const;  
```  
  
## Return Value  
 `TRUE` if the toolbar buttons display text labels below images; otherwise `FALSE`.  
  
## Remarks  
 Use [CMFCToolBar::EnableTextLabels](../vs140/CMFCToolBar--EnableTextLabels.md) to specify whether the text is displayed. The default value is `FALSE`. Call [CMFCToolBar::AllowChangeTextLabels](../vs140/CMFCToolBar--AllowChangeTextLabels.md) to specify whether the user can change this setting in the customization dialog box.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)