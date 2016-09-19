---
title: "CWnd::OnEndSession"
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
ms.assetid: e90c94a3-5589-41c7-8f13-464a1351075d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnEndSession
The framework calls this member function after the `CWnd` object has returned a nonzero value from a [OnQueryEndSession](../vs140/CWnd--OnQueryEndSession.md) member function call.  
  
## Syntax  
  
```  
  
      afx_msg void OnEndSession(  
   BOOL bEnding   
);  
```  
  
#### Parameters  
 `bEnding`  
 Specifies whether or not the session is being ended. It is **TRUE** if the session is being ended; otherwise **FALSE**.  
  
## Remarks  
 The `OnEndSession` call informs the `CWnd` object whether the session is actually ending.  
  
 If `bEnding` is **TRUE**, Windows can terminate any time after all applications have returned from processing this call. Consequently, have an application perform all tasks required for termination within `OnEndSession`.  
  
 You do not need to call the [DestroyWindow](../vs140/CWnd--DestroyWindow.md) member function or [PostQuitMessage](http://msdn.microsoft.com/library/windows/desktop/ms644945) Windows function when the session is ending.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DestroyWindow](../vs140/CWnd--DestroyWindow.md)   
 [CWnd::OnQueryEndSession](../vs140/CWnd--OnQueryEndSession.md)   
 [ExitWindows](http://msdn.microsoft.com/library/windows/desktop/aa376867)   
 [PostQuitMessage](http://msdn.microsoft.com/library/windows/desktop/ms644945)   
 [CWnd::OnQueryEndSession](../vs140/CWnd--OnQueryEndSession.md)   
 [CWnd::Default](../vs140/CWnd--Default.md)   
 [WM_ENDSESSION](http://msdn.microsoft.com/library/windows/desktop/aa376889)