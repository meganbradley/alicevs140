---
title: "CMDIChildWndEx::OnTaskbarTabThumbnailActivate"
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
ms.assetid: ee974bbc-5e33-48a0-8d00-72d5925afc1a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::OnTaskbarTabThumbnailActivate
Called by the framework when the Taskbar tab thumbnail should process the WM_ACTIVATE message.  
  
## Syntax  
  
```  
virtual void OnTaskbarTabThumbnailActivate(  
   UINT nState,  
   CWnd* pWndOther,  
   BOOL bMinimized  
);  
```  
  
#### Parameters  
 `nState`  
 Specifies whether the `CWnd` is being activated or deactivated.  
  
 `pWndOther`  
 Pointer to the `CWnd` being activated or deactivated. The pointer can be `NULL`, and it may be temporary.  
  
 `bMinimized`  
 Specifies the minimized state of the `CWnd` being activated or deactivated. A value of `TRUE` indicates the window is minimized.  
  
## Remarks  
 The default implementation activates the related MDI child frame.  
  
## Requirements  
 **Header:** afxmdichildwndex.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)