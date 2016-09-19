---
title: "CWinApp::PreTranslateMessage"
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
ms.assetid: dd11262e-7d32-44f1-8b9b-ed30daab88d7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::PreTranslateMessage
Override this function to filter window messages before they are dispatched to the Windows functions [TranslateMessage](http://msdn.microsoft.com/library/windows/desktop/ms644955) and [DispatchMessage](http://msdn.microsoft.com/library/windows/desktop/ms644934) The default implementation performs accelerator-key translation, so you must call the `CWinApp::PreTranslateMessage` member function in your overridden version.  
  
## Syntax  
  
```  
  
      virtual BOOL PreTranslateMessage(  
   MSG* pMsg   
);  
```  
  
#### Parameters  
 `pMsg`  
 A pointer to a [MSG](../vs140/MSG-Structure.md) structure that contains the message to process.  
  
## Return Value  
 Nonzero if the message was fully processed in `PreTranslateMessage` and should not be processed further. Zero if the message should be processed in the normal way.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [DispatchMessage](http://msdn.microsoft.com/library/windows/desktop/ms644934)   
 [TranslateMessage](http://msdn.microsoft.com/library/windows/desktop/ms644955)