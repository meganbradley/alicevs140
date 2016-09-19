---
title: "CWindow::SendMessage"
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
ms.assetid: 7c5c3a12-fb7e-422a-8376-1ac91a5cdace
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SendMessage
Sends a message to the window and does not return until the window procedure has processed the message.  
  
## Syntax  
  
```  
  
      LRESULT SendMessage(  
   UINT message,  
   WPARAM wParam = 0,  
   LPARAM lParam = 0   
) throw();  
static LRESULT SendMessage(  
   HWND hWnd,  
   UINT message,  
   WPARAM wParam,  
   LPARAM lParam   
) throw();  
```  
  
## Remarks  
 See [SendMessage](http://msdn.microsoft.com/library/windows/desktop/ms644950) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#29](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#29)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::PostMessage](../vs140/CWindow--PostMessage.md)   
 [CWindow::SendNotifyMessage](../vs140/CWindow--SendNotifyMessage.md)   
 [CWindow::SendMessageToDescendants](../vs140/CWindow--SendMessageToDescendants.md)