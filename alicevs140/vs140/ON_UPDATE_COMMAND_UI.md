---
title: "ON_UPDATE_COMMAND_UI"
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
ms.assetid: c4de3c21-2d2e-4b89-a4ce-d0c0e2d9edc4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ON_UPDATE_COMMAND_UI
This macro indicates which function will handle a user-interface update command message.  
  
## Syntax  
  
```  
  
ON_UPDATE_COMMAND_UI(  
id  
,   
memberFxn )  
```  
  
#### Parameters  
 `id`  
 The message ID.  
  
 `memberFxn`  
 The name of the message-handler function to which the message is mapped.  
  
## Remarks  
 There should be exactly one `ON_UPDATE_COMMAND_UI` macro statement in your message map for every user-interface update command that must be mapped to a message-handler function.  
  
 For more information and examples, see [Message Handling and Mapping Topics](../vs140/Message-Handling-and-Mapping.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ON_MESSAGE](../vs140/ON_MESSAGE.md)   
 [ON_REGISTERED_MESSAGE](../vs140/ON_REGISTERED_MESSAGE.md)   
 [ON_CONTROL](../vs140/ON_CONTROL.md)   
 [ON_COMMAND](../vs140/ON_COMMAND.md)   
 [CCmdUI Class](../vs140/CCmdUI-Class.md)