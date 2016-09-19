---
title: "CWinThread::PostThreadMessage"
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
ms.assetid: 23b5c524-b0e3-402e-baf8-bed1ba4b2a3b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::PostThreadMessage
Called to post a user-defined message to another `CWinThread` object.  
  
## Syntax  
  
```  
  
      BOOL PostThreadMessage(  
   UINT message ,  
   WPARAM wParam,  
   LPARAM lParam   
);  
```  
  
#### Parameters  
 `message`  
 ID of the user-defined message.  
  
 `wParam`  
 First message parameter.  
  
 `lParam`  
 Second message parameter.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The posted message is mapped to the proper message handler by the message map macro `ON_THREAD_MESSAGE`.  
  
> [!NOTE]
>  When calling the Windows [PostThreadMessage](http://msdn.microsoft.com/library/windows/desktop/ms644946) function within an MFC application, the MFC message handlers are not called. For more information, see the Knowledge Base article, "PRB: MFC Message Handler Not Called with PostThreadMessage()" (Q142415).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [ON_THREAD_MESSAGE](../vs140/ON_THREAD_MESSAGE.md)