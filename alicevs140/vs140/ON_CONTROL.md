---
title: "ON_CONTROL"
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
ms.assetid: 2cb7ebdf-296b-4606-b191-3449835003db
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ON_CONTROL
Indicates which function will handle a custom-control notification message.  
  
## Syntax  
  
```  
  
ON_CONTROL(  
wNotifyCode  
,   
id  
,   
memberFxn )  
```  
  
#### Parameters  
 `wNotifyCode`  
 The notification code of the control.  
  
 `id`  
 The command ID.  
  
 `memberFxn`  
 The name of the message-handler function to which the command is mapped.  
  
## Remarks  
 Control notification messages are those sent from a control to its parent window.  
  
 There should be exactly one `ON_CONTROL` macro statement in your message map for every control notification message that must be mapped to a message-handler function.  
  
 For more information and examples, see [Message Handling and Mapping Topics](../vs140/Message-Handling-and-Mapping.md).  
  
## Requirements  
 **Header:** afxmsg_.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ON_MESSAGE](../vs140/ON_MESSAGE.md)   
 [ON_REGISTERED_MESSAGE](../vs140/ON_REGISTERED_MESSAGE.md)