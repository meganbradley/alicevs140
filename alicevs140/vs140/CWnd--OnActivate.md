---
title: "CWnd::OnActivate"
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
ms.assetid: 18191cc7-73c4-4546-b572-c3b280c9788d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnActivate
The framework calls this member function when a `CWnd` object is being activated or deactivated.  
  
## Syntax  
  
```  
  
      afx_msg void OnActivate(  
   UINT nState,  
   CWnd* pWndOther,  
   BOOL bMinimized   
);  
```  
  
#### Parameters  
 `nState`  
 Specifies whether the `CWnd` is being activated or deactivated. It can be one of the following values:  
  
-   **WA_INACTIVE** The window is being deactivated.  
  
-   **WA_ACTIVE** The window is being activated through some method other than a mouse click (for example, by use of the keyboard interface to select the window).  
  
-   **WA_CLICKACTIVE** The window is being activated by a mouse click.  
  
 *pWndOther*  
 Pointer to the `CWnd` being activated or deactivated. The pointer can be **NULL**, and it may be temporary.  
  
 *bMinimized*  
 Specifies the minimized state of the `CWnd` being activated or deactivated. A value of **TRUE** indicates the window is minimized.  
  
 If **TRUE**, the `CWnd` is being activated; otherwise deactivated.  
  
## Remarks  
 If the `CWnd` object is activated with a mouse click, it will also receive an [OnMouseActivate](../vs140/CWnd--OnMouseActivate.md) member function call.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnMouseActivate](../vs140/CWnd--OnMouseActivate.md)   
 [CWnd::OnNcActivate](../vs140/CWnd--OnNcActivate.md)   
 [WM_ACTIVATE](http://msdn.microsoft.com/library/windows/desktop/ms646274)