---
title: "CMFCPopupMenuBar::StartPopupMenuTimer"
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
ms.assetid: 9f6ae710-e203-48fa-aaf2-0f51f32d175e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenuBar::StartPopupMenuTimer
Starts the timer for a specified delayed popup menu button.  
  
## Syntax  
  
```  
void StartPopupMenuTimer(  
   CMFCToolBarMenuButton* pMenuButton,  
   int nDelayFactor = 1  
);  
```  
  
#### Parameters  
 [in] `pMenuButton`  
 Pointer to the menu button for which to set the delay timer.  
  
 [in] `nDelayFactor`  
 A delay factor, equal to at least one, to multiply by the standard menu delay time (generally between a half second and five seconds).  
  
## Remarks  
  
## Requirements  
 **Header:** afxpopupmenubar.h  
  
## See Also  
 [CMFCPopupMenuBar Class](../vs140/CMFCPopupMenuBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)