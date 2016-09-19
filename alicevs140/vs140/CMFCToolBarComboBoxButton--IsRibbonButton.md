---
title: "CMFCToolBarComboBoxButton::IsRibbonButton"
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
ms.assetid: a5adfabd-40b2-4df9-848b-0a9814e62c17
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::IsRibbonButton
Indicates whether the combo box button resides on a ribbon panel.  
  
## Syntax  
  
```  
BOOL IsRibbonButton() const;  
```  
  
## Return Value  
 Always `FALSE`.  
  
## Remarks  
 By default, this method always returns `FALSE`, which means the combo box button is never displayed on a ribbon panel.  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)