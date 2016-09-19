---
title: "CMFCTasksPane::OnPressForwardButton"
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
ms.assetid: ead367b6-0d5a-4153-9f6a-139a23508f36
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::OnPressForwardButton
Called by the framework when the user clicks the forward navigation button.  
  
## Syntax  
  
```  
virtual void OnPressForwardButton();  
```  
  
## Remarks  
 By default, the framework displays the page that the user viewed before clicking the **Back** button.  
  
 Override this method in a derived class to execute custom code when the user clicks the forward button.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)