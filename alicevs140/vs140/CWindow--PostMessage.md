---
title: "CWindow::PostMessage"
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
ms.assetid: f778a4c1-7ee2-4c77-8076-90fca2724a1d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::PostMessage
Places a message in the message queue associated with the thread that created the window.  
  
## Syntax  
  
```  
  
      BOOL PostMessage(  
   UINT message,  
   WPARAM wParam = 0,  
   LPARAM lParam = 0   
) throw();  
```  
  
## Remarks  
 See [PostMessage](http://msdn.microsoft.com/library/windows/desktop/ms644944) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 Returns without waiting for the thread to process the message.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#27](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#27)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SendMessage](../vs140/CWindow--SendMessage.md)   
 [CWindow::SendNotifyMessage](../vs140/CWindow--SendNotifyMessage.md)