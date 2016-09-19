---
title: "CMFCToolBarMenuButton::SetTearOff"
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
ms.assetid: beb6943a-14ca-4331-ae72-b59849361517
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::SetTearOff
Specifies the ID of the tear-off bar for the drop-down menu.  
  
## Syntax  
  
```  
virtual void SetTearOff(  
   UINT uiBarID   
);  
```  
  
#### Parameters  
 [in] `uiBarID`  
 Specifies a new tear-off bar ID.  
  
## Remarks  
 Call this method to specify the ID for the tear-off bar that is created when the user drags the menu button off of a menu bar. If the `uiBarID` parameter is 0, the user cannot tear off the menu button.  
  
 Call [CWinAppEx::EnableTearOffMenus](../vs140/CWinAppEx--EnableTearOffMenus.md) to enable the tear-off menu feature in your application.  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)