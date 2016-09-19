---
title: "CMFCToolBarButton::OnCancelMode"
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
ms.assetid: a8c6ce24-1946-4c19-a400-deac624c9172
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::OnCancelMode
Called by the framework to handle the [WM_CANCELMODE](http://msdn.microsoft.com/library/windows/desktop/ms632615) message.  
  
## Syntax  
  
```  
virtual void OnCancelMode();  
```  
  
## Remarks  
 The default implementation of this method does nothing. Override this method if you want to handle the [WM_CANCELMODE](http://msdn.microsoft.com/library/windows/desktop/ms632615) message.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [WM_CANCELMODE](http://msdn.microsoft.com/library/windows/desktop/ms632615)