---
title: "CWinThread::GetMainWnd"
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
ms.assetid: 85e70750-4e26-4d35-a8a8-c1d58db10ce7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::GetMainWnd
If your application is an OLE server, call this function to retrieve a pointer to the active main window of the application instead of directly referring to the `m_pMainWnd` member of the application object.  
  
## Syntax  
  
```  
  
virtual CWnd * GetMainWnd( );  
```  
  
## Return Value  
 This function returns a pointer to one of two types of windows. If your thread is part of an OLE server and has an object that is in-place active inside an active container, this function returns the [CWinApp::m_pActiveWnd](../vs140/CWinApp--m_pActiveWnd.md) data member of the `CWinThread` object.  
  
 If there is no object that is in-place active within a container or your application is not an OLE server, this function returns the [m_pMainWnd](../vs140/CWinThread--m_pMainWnd.md) data member of your thread object.  
  
## Remarks  
 For user-interface threads, this is equivalent to directly referring to the `m_pActiveWnd` member of your application object.  
  
 If your application is not an OLE server, then calling this function is equivalent to directly referring to the `m_pMainWnd` member of your application object.  
  
 Override this function to modify the default behavior.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [AfxGetMainWnd](../vs140/AfxGetMainWnd.md)