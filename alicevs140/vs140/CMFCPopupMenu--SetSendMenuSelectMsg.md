---
title: "CMFCPopupMenu::SetSendMenuSelectMsg"
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
ms.assetid: 240b8612-48f4-4126-b3b5-0f309e117b88
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::SetSendMenuSelectMsg
Sets a flag that controls whether the pop-up menu notifies its parent frame when the user selects a command.  
  
## Syntax  
  
```  
static void SetSendMenuSelectMsg(  
   BOOL bSet = TRUE  
);  
```  
  
#### Parameters  
 [in] `bSet`  
 `TRUE` if the pop-up menu notifies its parent frame, `FALSE` otherwise.  
  
## Remarks  
 This is a global option for all the pop-up menus in an application. If it is enabled, the pop-up menus will send a `WM_MENUSELECT` message to the parent frame when the user selects a command.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)