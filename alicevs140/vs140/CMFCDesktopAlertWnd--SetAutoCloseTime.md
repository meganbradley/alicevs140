---
title: "CMFCDesktopAlertWnd::SetAutoCloseTime"
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
ms.assetid: 97a00476-fcda-4f3f-ac06-abbb5d2e844e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDesktopAlertWnd::SetAutoCloseTime
Sets the auto-close time out.  
  
## Syntax  
  
```  
void SetAutoCloseTime(  
    int nTime   
);  
```  
  
#### Parameters  
 [in] `nTime`  
 The time, in milliseconds, that elapses before the alert window automatically closes.  
  
## Remarks  
 The alert window is automatically closed after the specified time if the user does not interact with the window.  
  
## Requirements  
 **Header:** afxDesktopAlertWnd.h  
  
## See Also  
 [CMFCDesktopAlertWnd Class](../vs140/CMFCDesktopAlertWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)