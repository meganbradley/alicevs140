---
title: "CMFCToolBar::IsLastCommandFromButton"
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
ms.assetid: 6f93f2ab-719d-4f0b-a5a7-b202e1b3a218
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::IsLastCommandFromButton
Determines whether the most recently executed command was sent from the specified toolbar button.  
  
## Syntax  
  
```  
static BOOL IsLastCommandFromButton(  
   CMFCToolBarButton* pButton   
);  
```  
  
#### Parameters  
 [in] `pButton`  
 Pointer to button.  
  
## Return Value  
 `TRUE` if the last command was sent from the button that `pButton` specifies; otherwise `FALSE`.  
  
## Remarks  
 This method obtains a pointer to a [MSG Structure](../vs140/MSG-Structure.md) by calling `CWnd::GetCurrentMessage`. It then compares the `HWND` of the button with the `MSG::lParam` and `MSG::hwnd` members to determine whether the button was the source of the command.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)