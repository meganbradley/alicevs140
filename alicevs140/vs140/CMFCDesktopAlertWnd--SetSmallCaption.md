---
title: "CMFCDesktopAlertWnd::SetSmallCaption"
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
ms.assetid: f246f63e-b56a-4a0f-8364-6f7aa089a450
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDesktopAlertWnd::SetSmallCaption
Switches between small and regular-size captions.  
  
## Syntax  
  
```  
void SetSmallCaption(  
    BOOL bSmallCaption = TRUE  
);  
```  
  
#### Parameters  
 [in] `bSmallCaption`  
 `TRUE` to specify that the alert window displays a small caption; otherwise, `FALSE` to specify that the alert window displays a regular-size caption.  
  
## Remarks  
 Call this method to display the small or regular-size caption. By default, the small caption is 7 pixels high. You can obtain the size of the regular caption by calling the Windows API function `GetSystemMetrics(SM_CYCAPTION)`.  
  
## Requirements  
 **Header:** afxDesktopAlertWnd.h  
  
## See Also  
 [CMFCDesktopAlertWnd Class](../vs140/CMFCDesktopAlertWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)