---
title: "MessageHandler"
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
ms.topic: article
ms.assetid: 8a0acf97-1b0d-4226-91b9-75446634a03c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MessageHandler
**MessageHandler** is the name of the function identified by the second parameter of the `MESSAGE_HANDLER` macro in your message map.  
  
## Syntax  
  
```  
  
      LRESULT   
      MessageHandler  
      (  
   UINT uMsg,  
   WPARAM wParam,  
   LPARAM lParam,  
   BOOL& bHandled  
);  
```  
  
#### Parameters  
 `uMsg`  
 Specifies the message.  
  
 `wParam`  
 Additional message-specific information.  
  
 `lParam`  
 Additional message-specific information.  
  
 `bHandled`  
 The message map sets `bHandled` to **TRUE** before `MessageHandler` is called. If `MessageHandler` does not fully handle the message, it should set `bHandled` to **FALSE** to indicate the message needs further processing.  
  
## Return Value  
 The result of message processing. 0 if successful.  
  
## Remarks  
 For an example of using this message handler in a message map, see [MESSAGE_HANDLER](../vs140/MESSAGE_HANDLER.md).  
  
## See Also  
 [Implementing a Window](../vs140/Implementing-a-Window.md)   
 [Message Maps](../vs140/Message-Maps--ATL-.md)   
 [WM_NOTIFY](http://msdn.microsoft.com/library/windows/desktop/bb775583)