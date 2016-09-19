---
title: "CMFCToolBar::OnReset"
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
ms.assetid: 41593e7f-a345-4d84-8ad3-c24b327c969d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::OnReset
Restores the toolbar to its original state.  
  
## Syntax  
  
```  
virtual void OnReset();  
```  
  
## Remarks  
 Override this method to handle notification about a toolbar reset.  
  
 The default implementation does nothing. Override `OnReset` in a class derived from [CMFCToolBar](../Topic/CMFCToolBar%20Class.md) when the toolbar has dummy buttons that must be replaced when the toolbar returns to its original state.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)