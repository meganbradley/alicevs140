---
title: "CMFCTasksPane::OnPressBackButton"
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
ms.assetid: e799fa7b-a02c-41fa-b75a-22a7710ea77a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::OnPressBackButton
Called by the framework when the user clicks the back button.  
  
## Syntax  
  
```  
virtual void OnPressBackButton();  
```  
  
## Remarks  
 By default, the framework displays the previously viewed page.  
  
 Override this method in a derived class to execute custom code when the user clicks the back button.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)