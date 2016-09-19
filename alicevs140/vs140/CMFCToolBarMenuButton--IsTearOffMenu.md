---
title: "CMFCToolBarMenuButton::IsTearOffMenu"
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
ms.assetid: e9dbd416-f8ce-472a-b293-0b905a18692c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::IsTearOffMenu
Indicates whether the drop-down menu has a tear-off bar.  
  
## Syntax  
  
```  
virtual BOOL IsTearOffMenu() const;  
```  
  
## Return Value  
 `TRUE` if the toolbar menu button has a tear-off bar; otherwise `FALSE`.  
  
## Remarks  
 To enable the tear-off feature and set the tear-off bar ID, call [CMFCToolBarMenuButton::SetTearOff](../vs140/CMFCToolBarMenuButton--SetTearOff.md).  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)