---
title: "CMFCToolBarMenuButton::SetRadio"
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
ms.assetid: f003c23a-caa6-4aec-b220-dc5308fd85fe
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::SetRadio
Sets the toolbar menu button to display a radio button style icon when it is checked.  
  
## Syntax  
  
```  
virtual void SetRadio();  
```  
  
## Remarks  
 When the menu button is drawn while it is checked, it calls [CMFCVisualManager::OnDrawMenuCheck](../vs140/CMFCVisualManager--OnDrawMenuCheck.md) to draw a checkmark icon. By default, `OnDrawMenuCheck` requests that the current visual manager draws a checkbox style checkmark on the menu button. After you call this method, the current visual manager instead draws a radio button style checkmark on the menu button. This change cannot be undone.  
  
 When you call this method and the menu button is currently being displayed, it will refresh.  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)