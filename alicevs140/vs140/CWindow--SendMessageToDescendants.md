---
title: "CWindow::SendMessageToDescendants"
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
ms.assetid: 2e60ecd5-4191-4cb9-b075-e95d9f468c0f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SendMessageToDescendants
Sends the specified message to all immediate children of the `CWindow` object.  
  
## Syntax  
  
```  
  
      void SendMessageToDescendants(  
   UINT message,  
   WPARAM wParam = 0,  
   LPARAM lParam = 0,  
   BOOL bDeep = TRUE   
) throw();  
```  
  
#### Parameters  
 `message`  
 [in] The message to be sent.  
  
 `wParam`  
 [in] Additional message-specific information.  
  
 `lParam`  
 [in] Additional message-specific information.  
  
 `bDeep`  
 [in] If **TRUE** (the default value), the message will be sent to all descendant windows; otherwise, it will be sent only to the immediate child windows.  
  
## Remarks  
 If `bDeep` is **TRUE**, the message is additionally sent to all other descendant windows.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SendMessage](../vs140/CWindow--SendMessage.md)   
 [CWindow::SendNotifyMessage](../vs140/CWindow--SendNotifyMessage.md)   
 [CWindow::PostMessage](../vs140/CWindow--PostMessage.md)