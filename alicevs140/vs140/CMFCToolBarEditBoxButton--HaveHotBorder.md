---
title: "CMFCToolBarEditBoxButton::HaveHotBorder"
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
ms.assetid: 2a2beffd-17e3-4da4-bf38-587fdd7bec94
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::HaveHotBorder
Determines whether a border of the button is displayed when a user clicks the button.  
  
## Syntax  
  
```  
virtual BOOL HaveHotBorder() const;  
```  
  
## Return Value  
 Nonzero if a button displays its border when selected; otherwise 0.  
  
## Remarks  
 This method extends the base class implementation, [CMFCToolBarButton::HaveHotBorder](../vs140/CMFCToolBarButton--HaveHotBorder.md), by returning a nonzero value if the control is visible.  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::HaveHotBorder](../vs140/CMFCToolBarButton--HaveHotBorder.md)