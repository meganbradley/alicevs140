---
title: "CWnd::PostMessage"
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
ms.assetid: 3f7f2cd5-07ac-43a1-81cd-5ad39f3c8229
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::PostMessage
Places a message in the window's message queue and then returns without waiting for the corresponding window to process the message.  
  
## Syntax  
  
```  
  
      BOOL PostMessage(  
   UINT message,  
   WPARAM wParam = 0,  
   LPARAM lParam = 0   
);  
```  
  
#### Parameters  
 `message`  
 Specifies the message to be posted.  
  
 `wParam`  
 Specifies additional message information. The content of this parameter depends on the message being posted.  
  
 `lParam`  
 Specifies additional message information. The content of this parameter depends on the message being posted.  
  
## Return Value  
 Nonzero if the message is posted; otherwise 0.  
  
## Remarks  
 Messages in a message queue are retrieved by calls to the [GetMessage](http://msdn.microsoft.com/library/windows/desktop/ms644936) or [PeekMessage](http://msdn.microsoft.com/library/windows/desktop/ms644943) Windows function.  
  
 The Windows [PostMessage](http://msdn.microsoft.com/library/windows/desktop/ms644944) function can be used to access another application.  
  
## Example  
 See the example for [AfxGetMainWnd](../vs140/AfxGetMainWnd.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [GetMessage](http://msdn.microsoft.com/library/windows/desktop/ms644936)   
 [PeekMessage](http://msdn.microsoft.com/library/windows/desktop/ms644943)   
 [PostMessage](http://msdn.microsoft.com/library/windows/desktop/ms644944)   
 [PostThreadMessage](http://msdn.microsoft.com/library/windows/desktop/ms644946)   
 [CWnd::SendMessage](../vs140/CWnd--SendMessage.md)