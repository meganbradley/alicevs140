---
title: "NotifyHandler"
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
ms.assetid: 5ff953ec-de35-42bc-8b3c-d384d636c139
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NotifyHandler
The name of the function identified by the third parameter of the `NOTIFY_HANDLER` macro in your message map.  
  
## Syntax  
  
```  
  
      LRESULT   
      NotifyHandler  
      (  
   int idCtrl,  
   LPNMHDR pnmh,  
   BOOL& bHandled   
);  
```  
  
#### Parameters  
 `idCtrl`  
 The identifier of the control sending the message.  
  
 *pnmh*  
 Address of an [NMHDR](http://msdn.microsoft.com/library/windows/desktop/bb775514) structure that contains the notification code and additional information. For some notification messages, this parameter points to a larger structure that has the **NMHDR** structure as its first member.  
  
 `bHandled`  
 The message map sets `bHandled` to **TRUE** before *NotifyHandler* is called. If *NotifyHandler* does not fully handle the message, it should set `bHandled` to **FALSE** to indicate the message needs further processing.  
  
## Return Value  
 The result of message processing. 0 if successful.  
  
## Remarks  
 For an example of using this message handler in a message map, see [NOTIFY_HANDLER](../vs140/NOTIFY_HANDLER.md).  
  
## See Also  
 [Implementing a Window](../vs140/Implementing-a-Window.md)   
 [Message Maps](../vs140/Message-Maps--ATL-.md)   
 [WM_NOTIFY](http://msdn.microsoft.com/library/windows/desktop/bb775583)