---
title: "CWnd::OnNcRButtonDblClk"
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
ms.assetid: 8de2e69b-1a95-4c3c-9966-0a48fcc5cae3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnNcRButtonDblClk
The framework calls this member function when the user double-clicks the right mouse button while the cursor is within a nonclient area of `CWnd`.  
  
## Syntax  
  
```  
  
      afx_msg void OnNcRButtonDblClk(  
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
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnNcHitTest](../vs140/CWnd--OnNcHitTest.md)   
 [CWnd::OnNcRButtonDown](../vs140/CWnd--OnNcRButtonDown.md)   
 [CWnd::OnNcRButtonUp](../vs140/CWnd--OnNcRButtonUp.md)   
 [CWnd::OnNcRButtonDblClk](../vs140/CWnd--OnNcRButtonDblClk.md)