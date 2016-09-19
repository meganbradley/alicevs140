---
title: "CMFCToolBarMenuButton::IsExclusive"
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
ms.assetid: d8ee778f-83b2-4596-b139-c64567a26311
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::IsExclusive
Indicates whether the button is in exclusive mode.  
  
## Syntax  
  
```  
virtual BOOL IsExclusive() const;  
```  
  
## Return Value  
 `TRUE` if the button is working in exclusive mode; otherwise `FALSE`.  
  
## Remarks  
 When a user opens a popup menu for a button and then moves the mouse pointer over another toolbar or menu button, the popup menu closes unless the button is in exclusive mode.  
  
 The default implementation always returns `FALSE`. Override this method in a derived class if you want to turn on exclusive mode.  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)