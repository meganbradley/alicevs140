---
title: "CWinThread::PreTranslateMessage"
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
ms.assetid: d726346b-2f3c-4f0e-9bb2-d67084ce4b21
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::PreTranslateMessage
Override this function to filter window messages before they are dispatched to the Windows functions [TranslateMessage](http://msdn.microsoft.com/library/windows/desktop/ms644955) and [DispatchMessage](http://msdn.microsoft.com/library/windows/desktop/ms644934).  
  
## Syntax  
  
```  
  
      virtual BOOL PreTranslateMessage(  
   MSG *pMsg   
);  
```  
  
#### Parameters  
 `pMsg`  
 Points to a [MSG](../vs140/MSG-Structure.md) structure containing the message to process.  
  
## Return Value  
 Nonzero if the message was fully processed in `PreTranslateMessage` and should not be processed further. Zero if the message should be processed in the normal way.  
  
## Remarks  
 This member function is used only in user-interface threads.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::PreTranslateMessage](../vs140/CWinApp--PreTranslateMessage.md)