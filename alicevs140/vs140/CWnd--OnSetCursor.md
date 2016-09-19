---
title: "CWnd::OnSetCursor"
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
ms.assetid: 72898ddb-9d5f-4277-9023-6dad34bf24b6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnSetCursor
The framework calls this member function if mouse input is not captured and the mouse causes cursor movement within the `CWnd` object.  
  
## Syntax  
  
```  
  
      afx_msg BOOL OnSetCursor(  
   CWnd* pWnd,  
   UINT nHitTest,  
   UINT message   
);  
```  
  
#### Parameters  
 `pWnd`  
 Specifies a pointer to the window that contains the cursor. The pointer may be temporary and should not be stored for later use.  
  
 `nHitTest`  
 Specifies the [hit-test](../vs140/CWnd--OnNcHitTest.md) area code. The hit test determines the cursor's location.  
  
 `message`  
 Specifies the mouse message number.  
  
## Return Value  
 Nonzero to halt further processing, or 0 to continue.  
  
## Remarks  
 The default implementation calls the parent window's `OnSetCursor` before processing. If the parent window returns **TRUE**, further processing is halted. Calling the parent window gives the parent window control over the cursor's setting in a child window.  
  
 The default implementation sets the cursor to an arrow if it is not in the client area or to the registered-class cursor if it is.  
  
 If `nHitTest` is **HTERROR** and `message` is a mouse button-down message, the **MessageBeep** member function is called.  
  
 The `message` parameter is 0 when `CWnd` enters menu mode.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnNcHitTest](../vs140/CWnd--OnNcHitTest.md)   
 [WM_SETCURSOR](http://msdn.microsoft.com/library/windows/desktop/ms648382)   
 [How Do I: Change the Mouse Cursor in an Microsoft Foundation Class Application?](http://go.microsoft.com/fwlink/?LinkID=128044)