---
title: "ON_MESSAGE"
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
ms.assetid: e2faeb13-9f6e-4c0d-9f6d-b2e141a0db1e
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ON_MESSAGE
Indicates which function will handle a user-defined message.  
  
## Syntax  
  
```  
  
ON_MESSAGE(  
message  
,   
memberFxn  
)  
  
```  
  
#### Parameters  
 `message`  
 The message ID.  
  
 `memberFxn`  
 The name of the message-handler function to which the message is mapped.  
  
 The type of the function must be `afx_msg LRESULT (CWnd::*)(WPARAM, LPARAM)`.  
  
## Remarks  
 User-defined messages are any messages that are not standard Windows `WM_MESSAGE` messages. When selecting a message ID, you must use values within the range of `WM_USER` (0x0400) to 0x7FFF or `WM_APP` (0x8000) to 0xBFFF. For more information regarding message IDs, see [WM_APP](http://msdn.microsoft.com/library/windows/desktop/ms644930).  
  
 There should be exactly one `ON_MESSAGE` macro statement in your message map for every user-defined message that must be mapped to a message-handler function.  
  
> [!NOTE]
>  In addition to user-defined messages, `ON_MESSAGE` handles less common Windows messages. For more information, see Knowledge Base article [99848: INFO: Use ON_MESSAGE() Macro to Map Less-Common Messages](http://go.microsoft.com/fwlink/?linkId=192022).  
  
 For more information and examples, see [Message Handling and Mapping Topics](../vs140/Message-Handling-and-Mapping.md) and [User-Defined Handlers](../vs140/User-Defined-Handlers.md)  
  
## Example  
 [!CODE [NVC_MFCMessageMaps#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCMessageMaps#4)]  
  
 [!CODE [NVC_MFCMessageMaps#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCMessageMaps#5)]  
  
 [!CODE [NVC_MFCMessageMaps#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCMessageMaps#3)]  
  
 [!CODE [NVC_MFCMessageMaps#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCMessageMaps#14)]  
  
## Requirements  
 **Header:** afxmsg_.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ON_UPDATE_COMMAND_UI](../vs140/ON_UPDATE_COMMAND_UI.md)   
 [ON_CONTROL](../vs140/ON_CONTROL.md)   
 [ON_REGISTERED_MESSAGE](../vs140/ON_REGISTERED_MESSAGE.md)   
 [ON_COMMAND](../vs140/ON_COMMAND.md)