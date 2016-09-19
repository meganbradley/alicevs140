---
title: "CWnd::OnNcLButtonDown"
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
ms.assetid: 77585fd3-6478-41c8-9dd2-145b06c6e9d2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnNcLButtonDown
The framework calls this member function when the user presses the left mouse button while the cursor is within a nonclient area of the `CWnd` object.  
  
## Syntax  
  
```  
  
      afx_msg void OnNcLButtonDown(  
   UINT nHitTest,  
   CPoint point   
);  
```  
  
#### Parameters  
 `nHitTest`  
 Specifies the [hit-test code](../vs140/CWnd--OnNcHitTest.md). A hit test is a test that determines the location of the cursor.  
  
 `point`  
 Specifies a `CPoint` object that contains the x and y screen coordinates of the cursor position. These coordinates are always relative to the upper-left corner of the screen.  
  
## Remarks  
 If appropriate, the [WM_SYSCOMMAND](../vs140/CWnd--OnSysCommand.md) is sent.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received.If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnNcHitTest](../vs140/CWnd--OnNcHitTest.md)   
 [CWnd::OnNcLButtonDblClk](../vs140/CWnd--OnNcLButtonDblClk.md)   
 [CWnd::OnNcLButtonUp](../vs140/CWnd--OnNcLButtonUp.md)   
 [CWnd::OnSysCommand](../vs140/CWnd--OnSysCommand.md)   
 [WM_NCLBUTTONDOWN](http://msdn.microsoft.com/library/windows/desktop/ms645620)   
 [CWnd::Default](../vs140/CWnd--Default.md)