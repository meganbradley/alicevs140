---
title: "MESSAGE_HANDLER"
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
ms.assetid: 0253a7f3-7eb3-4d2d-83b9-060161268d04
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MESSAGE_HANDLER
Defines an entry in a message map.  
  
## Syntax  
  
```  
  
      MESSAGE_HANDLER(   
   msg,   
   func    
)  
```  
  
#### Parameters  
 `msg`  
 [in] The Windows message.  
  
 `func`  
 [in] The name of the message-handler function.  
  
## Remarks  
 `MESSAGE_HANDLER` maps a Windows message to the specified handler function.  
  
 Any function specified in a `MESSAGE_HANDLER` macro must be defined as follows:  
  
 `LRESULT MessageHandler(UINT uMsg, WPARAM wParam, LPARAM lParam, BOOL& bHandled);`  
  
 The message map sets `bHandled` to **TRUE** before `MessageHandler` is called. If `MessageHandler` does not fully handle the message, it should set `bHandled` to **FALSE** to indicate the message needs further processing.  
  
> [!NOTE]
>  Always begin a message map with [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md). You can then declare subsequent alternate message maps with [ALT_MSG_MAP](../vs140/ALT_MSG_MAP.md). The [END_MSG_MAP](../vs140/END_MSG_MAP.md) macro marks the end of the message map. Every message map must have exactly one instance of `BEGIN_MSG_MAP` and `END_MSG_MAP`.  
  
 In addition to `MESSAGE_HANDLER`, you can use [COMMAND_HANDLER](../vs140/COMMAND_HANDLER.md) and [NOTIFY_HANDLER](../vs140/NOTIFY_HANDLER.md) to map [WM_COMMAND](http://msdn.microsoft.com/library/windows/desktop/ms647591) and [WM_NOTIFY](http://msdn.microsoft.com/library/windows/desktop/bb775583) messages, respectively.  
  
 For more information about using message maps in ATL, see [Message Maps](../vs140/Message-Maps--ATL-.md).  
  
## Example  
 [!CODE [NVC_ATL_Windowing#129](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#129)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [MESSAGE_RANGE_HANDLER](../vs140/MESSAGE_RANGE_HANDLER.md)