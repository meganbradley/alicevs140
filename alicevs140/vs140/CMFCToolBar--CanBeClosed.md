---
title: "CMFCToolBar::CanBeClosed"
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
ms.assetid: f2e642b1-57df-4476-9d00-b11da0044351
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::CanBeClosed
Specifies whether a user can close the toolbar.  
  
## Syntax  
  
```  
virtual BOOL CanBeClosed() const;  
```  
  
## Return Value  
 `TRUE` if the toolbar can be closed by the user; otherwise `FALSE`.  
  
## Remarks  
 The framework calls this method to determine whether the user can close a toolbar. If the method returns `TRUE`, the framework enables the SC_CLOSE command in the system menu of the toolbar and the user can close the toolbar by using a check box in the list of toolbars in the customization dialog box.  
  
 The default implementation returns `TRUE`. Override this method in a class derived from [CMFCToolBar](../Topic/CMFCToolBar%20Class.md) to make toolbar objects that cannot be closed by the user.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)