---
title: "CMFCDropDownToolbarButton::IsDropDown"
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
ms.assetid: 01230fa0-dc16-4d2c-aea6-f17a621586e8
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::IsDropDown
Determines whether the drop-down toolbar is currently open.  
  
## Syntax  
  
```  
BOOL IsDropDown() const;  
```  
  
## Return Value  
 Nonzero if the drop-down toolbar is currently open; otherwise 0.  
  
## Remarks  
 The framework opens the drop-down toolbar by using the [CMFCDropDownToolbarButton::DropDownToolbar](../vs140/CMFCDropDownToolbarButton--DropDownToolbar.md) method. The framework closes the drop-down toolbar when the user presses the left-mouse button in the non-client area of the drop-down toolbar.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCDropDownToolbarButton::DropDownToolbar](../vs140/CMFCDropDownToolbarButton--DropDownToolbar.md)