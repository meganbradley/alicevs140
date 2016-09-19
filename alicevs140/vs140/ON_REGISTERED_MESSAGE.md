---
title: "ON_REGISTERED_MESSAGE"
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
ms.assetid: 93c1c068-ae8c-4e04-8a60-a603800ab57d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ON_REGISTERED_MESSAGE
The Windows **RegisterWindowMessage** function is used to define a new window message that is guaranteed to be unique throughout the system.  
  
## Syntax  
  
```  
  
ON_REGISTERED_MESSAGE(  
nMessageVariable  
,   
memberFxn )  
```  
  
#### Parameters  
 `nMessageVariable`  
 The registered window-message ID variable.  
  
 `memberFxn`  
 The name of the message-handler function to which the message is mapped.  
  
## Remarks  
 This macro indicates which function will handle the registered message.  
  
 For more information and examples, see [Message Handling and Mapping Topics](../vs140/Message-Handling-and-Mapping.md).  
  
## Example  
 [!CODE [NVC_MFCMessageMaps#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCMessageMaps#8)]  
  
 [!CODE [NVC_MFCMessageMaps#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCMessageMaps#15)]  
  
## Requirements  
 **Header:** afxmsg_.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ON_MESSAGE](../vs140/ON_MESSAGE.md)   
 [ON_UPDATE_COMMAND_UI](../vs140/ON_UPDATE_COMMAND_UI.md)   
 [ON_CONTROL](../vs140/ON_CONTROL.md)   
 [ON_COMMAND](../vs140/ON_COMMAND.md)   
 [RegisterWindowMessage](http://msdn.microsoft.com/library/windows/desktop/ms644947)   
 [User-Defined Handlers](../vs140/User-Defined-Handlers.md)