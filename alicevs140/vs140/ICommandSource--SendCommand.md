---
title: "ICommandSource::SendCommand"
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
ms.assetid: be347ba3-a9d7-48a4-9020-86d0be0f8956
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandSource::SendCommand
Sends a message and waits for it to be processed before returning.  
  
## Syntax  
  
```  
void SendCommand(   
   unsigned int command   
);  
```  
  
#### Parameters  
 `command`  
 The command ID of the message to be sent.  
  
## Remarks  
 This method synchronously sends the message mapped to the ID specified by `command`. It calls [CWnd::SendMessage](../vs140/CWnd--SendMessage.md) to place the message in the window's message queue and waits until that window procedure has processed the message before returning.  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 [ICommandSource Interface](../vs140/ICommandSource-Interface.md)   
 [ICommandSource::PostCommand](../vs140/ICommandSource--PostCommand.md)