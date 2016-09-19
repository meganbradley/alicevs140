---
title: "CDockingManager::OnClosePopupMenu"
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
ms.assetid: e49e8536-6fa4-438b-945c-753200ec7442
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::OnClosePopupMenu
Called by the framework when an active pop-up menu processes a WM_DESTROY message.  
  
## Syntax  
  
```  
void OnClosePopupMenu();  
```  
  
## Remarks  
 The framework sends a WM_DESTROY message when it is about to close the current main window. Override this method to handle notifications from `CMFCPopupMenu` objects that belong to the frame window when a `CMFCPopupMenu` object processes a `WM_DESTROY` message.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)