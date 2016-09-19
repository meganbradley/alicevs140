---
title: "CMDIChildWndEx::OnTaskbarTabThumbnailMouseActivate"
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
ms.assetid: 14a5cdea-54cb-4c8f-bf28-cbcc1a5e5ac3
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::OnTaskbarTabThumbnailMouseActivate
Called by the framework when the Taskbar tab thumbnail should process the WM_MOUSEACTIVATE message.  
  
## Syntax  
  
```  
virtual int OnTaskbarTabThumbnailMouseActivate(  
   CWnd* pDesktopWnd,  
   UINT nHitTest,  
   UINT message  
);  
```  
  
#### Parameters  
 `pDesktopWnd`  
 Specifies a pointer to the top-level parent window of the window being activated. The pointer may be temporary and should not be stored.  
  
 `nHitTest`  
 Specifies the hit-test area code. A hit test is a test that determines the location of the cursor.  
  
 `message`  
 Specifies the mouse message number.  
  
## Remarks  
 The default implementation activates the related MDI child frame.  
  
## Requirements  
 **Header:** afxmdichildwndex.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)