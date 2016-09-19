---
title: "CMFCToolBarButton::GetHwnd"
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
ms.assetid: 301a5c3e-0ca3-4705-999a-bba7bcb376e5
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::GetHwnd
Retrieves the window handle that is associated with the toolbar button.  
  
## Syntax  
  
```  
virtual HWND GetHwnd();  
```  
  
## Return Value  
 The window handle that is associated with the toolbar button or `NULL` if the toolbar button has no associated window handle.  
  
## Remarks  
 The default implementation of this method returns `NULL`. Override this method to return the window handle of your specific control.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)