---
title: "CWinThread::InitInstance"
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
ms.assetid: 346176e4-9dcf-4d00-bee7-48b307328991
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::InitInstance
`InitInstance` must be overridden to initialize each new instance of a user-interface thread.  
  
## Syntax  
  
```  
  
virtual BOOL InitInstance( );  
```  
  
## Return Value  
 Nonzero if initialization is successful; otherwise 0.  
  
## Remarks  
 Typically, you override `InitInstance` to perform tasks that must be completed when a thread is first created.  
  
 This member function is used only in user-interface threads. Perform initialization of worker threads in the controlling function passed to [AfxBeginThread](../vs140/AfxBeginThread.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md)