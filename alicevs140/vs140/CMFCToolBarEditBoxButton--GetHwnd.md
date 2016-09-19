---
title: "CMFCToolBarEditBoxButton::GetHwnd"
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
ms.assetid: 699ef3c8-4651-4191-a55a-b48db814fb48
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::GetHwnd
Retrieves the window handle that is associated with the toolbar button.  
  
## Syntax  
  
```  
virtual HWND GetHwnd();  
```  
  
## Return Value  
 The window handle that is associated with the button.  
  
## Remarks  
 This method overrides the [CMFCToolBarButton::GetHwnd](../vs140/CMFCToolBarButton--GetHwnd.md) method by returning the window handle of the edit control part of the edit box button.  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::GetHwnd](../vs140/CMFCToolBarButton--GetHwnd.md)