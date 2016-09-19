---
title: "CMFCTasksPane::OnPressHomeButton"
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
ms.assetid: bdd8c35b-d0b7-4b08-8f18-a17fc16aebe0
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::OnPressHomeButton
Called by the framework when the user clicks the home navigation button.  
  
## Syntax  
  
```  
virtual void OnPressHomeButton();  
```  
  
## Remarks  
 By default, the framework displays the default page for the task group.  
  
 Override this method in a derived class to execute custom code when the user clicks the home navigation button.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)