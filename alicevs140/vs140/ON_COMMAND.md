---
title: "ON_COMMAND"
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
ms.assetid: f24f8bda-2cf4-49d5-aa3d-6f2e6bb003f2
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ON_COMMAND
This macro maps a command message to a member function.  
  
## Syntax  
  
```  
  
ON_COMMAND(  
id  
,   
memberFxn )  
```  
  
#### Parameters  
 `id`  
 The command ID.  
  
 `memberFxn`  
 The name of the message-handler function to which the command is mapped.  
  
## Remarks  
 It indicates which function will handle a command message from a command user-interface object such as a menu item or toolbar button.  
  
 When a command-target object receives a Windows **WM_COMMAND** message with the specified ID, `ON_COMMAND` will call the member function `memberFxn` to handle the message.  
  
 Use `ON_COMMAND` to map a single command to a member function. Use [ON_COMMAND_RANGE](../vs140/ON_COMMAND_RANGE.md) to map a range of command ids to one member function. Only one message-map entry can match a given command id. That is, you can't map a command to more than one handler. For more information and examples, see [Message Handling and Mapping Topics](../vs140/Message-Handling-and-Mapping.md).  
  
## Example  
 [!CODE [NVC_MFCListView#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCListView#11)]  
  
## Requirements  
 **Header:** afxmsg_.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ON_UPDATE_COMMAND_UI](../vs140/ON_UPDATE_COMMAND_UI.md)