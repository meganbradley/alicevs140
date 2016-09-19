---
title: "BEGIN_MSG_MAP"
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
ms.assetid: 8bbb5af9-18b1-48c6-880e-166f599ee554
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_MSG_MAP
Marks the beginning of the default message map.  
  
## Syntax  
  
```  
  
BEGIN_MSG_MAP( theClass )  
```  
  
#### Parameters  
 `theClass`  
 [in] The name of the class containing the message map.  
  
## Remarks  
 [CWindowImpl::WindowProc](../vs140/CWindowImpl--WindowProc.md) uses the default message map to process messages sent to the window. The message map directs messages either to the appropriate handler function or to another message map.  
  
 The following macros map a message to a handler function. This function must be defined in `theClass`.  
  
|Macro|Description|  
|-----------|-----------------|  
|[MESSAGE_HANDLER](../vs140/MESSAGE_HANDLER.md)|Maps a Windows message to a handler function.|  
|[MESSAGE_RANGE_HANDLER](../vs140/MESSAGE_RANGE_HANDLER.md)|Maps a contiguous range of Windows messages to a handler function.|  
|[COMMAND_HANDLER](../vs140/COMMAND_HANDLER.md)|Maps a **WM_COMMAND** message to a handler function, based on the notification code and the identifier of the menu item, control, or accelerator.|  
|[COMMAND_ID_HANDLER](../vs140/COMMAND_ID_HANDLER.md)|Maps a **WM_COMMAND** message to a handler function, based on the identifier of the menu item, control, or accelerator.|  
|[COMMAND_CODE_HANDLER](../vs140/COMMAND_HANDLER.md)|Maps a **WM_COMMAND** message to a handler function, based on the notification code.|  
|[COMMAND_RANGE_HANDLER](../vs140/COMMAND_RANGE_HANDLER.md)|Maps a contiguous range of **WM_COMMAND** messages to a handler function, based on the identifier of the menu item, control, or accelerator.|  
|[NOTIFY_HANDLER](../vs140/NOTIFY_HANDLER.md)|Maps a **WM_NOTIFY** message to a handler function, based on the notification code and the control identifier.|  
|[NOTIFY_ID_HANDLER](../vs140/NOTIFY_ID_HANDLER.md)|Maps a **WM_NOTIFY** message to a handler function, based on the control identifier.|  
|[NOTIFY_CODE_HANDLER](../vs140/NOTIFY_CODE_HANDLER.md)|Maps a **WM_NOTIFY** message to a handler function, based on the notification code.|  
|[NOTIFY_RANGE_HANDLER](../vs140/NOTIFY_RANGE_HANDLER.md)|Maps a contiguous range of **WM_NOTIFY** messages to a handler function, based on the control identifier.|  
  
 The following macros direct messages to another message map. This process is called "chaining."  
  
|Macro|Description|  
|-----------|-----------------|  
|[CHAIN_MSG_MAP](../vs140/CHAIN_MSG_MAP.md)|Chains to the default message map in the base class.|  
|[CHAIN_MSG_MAP_MEMBER](../vs140/CHAIN_MSG_MAP_MEMBER.md)|Chains to the default message map in a data member of the class.|  
|[CHAIN_MSG_MAP_ALT](../vs140/CHAIN_MSG_MAP_ALT.md)|Chains to an alternate message map in the base class.|  
|[CHAIN_MSG_MAP_ALT_MEMBER](../vs140/CHAIN_MSG_MAP_ALT_MEMBER.md)|Chains to an alternate message map in a data member of the class.|  
|[CHAIN_MSG_MAP_DYNAMIC](../vs140/CHAIN_MSG_MAP_DYNAMIC.md)|Chains to the default message map in another class at run time.|  
  
 The following macros direct "reflected" messages from the parent window. For example, a control normally sends notification messages to its parent window for processing, but the parent window can reflect the message back to the control.  
  
|Macro|Description|  
|-----------|-----------------|  
|[REFLECTED_COMMAND_HANDLER](../vs140/REFLECTED_COMMAND_HANDLER.md)|Maps a reflected **WM_COMMAND** message to a handler function, based on the notification code and the identifier of the menu item, control, or accelerator.|  
|[REFLECTED_COMMAND_ID_HANDLER](../vs140/REFLECTED_COMMAND_ID_HANDLER.md)|Maps a reflected **WM_COMMAND** message to a handler function, based on the identifier of the menu item, control, or accelerator.|  
|[REFLECTED_COMMAND_CODE_HANDLER](../vs140/REFLECTED_COMMAND_CODE_HANDLER.md)|Maps a reflected **WM_COMMAND** message to a handler function, based on the notification code.|  
|[REFLECTED_COMMAND_RANGE_HANDLER](../vs140/REFLECTED_COMMAND_RANGE_HANDLER.md)|Maps a reflected **WM_COMMAND** message to a handler function, based on a contiguous range of control identifiers.|  
|[REFLECTED_COMMAND_RANGE_CODE_HANDLER](../vs140/REFLECTED_COMMAND_RANGE_CODE_HANDLER.md)|Maps a reflected **WM_COMMAND** message to a handler function, based on the notification code and a contiguous range of control identifiers.|  
|[REFLECTED_NOTIFY_HANDLER](../vs140/REFLECTED_NOTIFY_HANDLER.md)|Maps a reflected **WM_NOTIFY** message to a handler function, based on the notification code and the control identifier.|  
|[REFLECTED_NOTIFY_ID_HANDLER](../vs140/REFLECTED_NOTIFY_ID_HANDLER.md)|Maps a reflected **WM_NOTIFY** message to a handler function, based on the control identifier.|  
|[REFLECTED_NOTIFY_CODE_HANDLER](../vs140/REFLECTED_NOTIFY_CODE_HANDLER.md)|Maps a reflected **WM_NOTIFY** message to a handler function, based on the notification code.|  
|[REFLECTED_NOTIFY_RANGE_HANDLER](../vs140/REFLECTED_NOTIFY_RANGE_HANDLER.md)|Maps a reflected **WM_NOTIFY** message to a handler function, based on a contiguous range of control identifiers.|  
|[REFLECTED_NOTIFY_RANGE_CODE_HANDLER](../vs140/REFLECTED_NOTIFY_RANGE_CODE_HANDLER.md)|Maps a reflected **WM_NOTIFY** message to a handler function, based on the notification code and a contiguous range of control identifiers.|  
  
## Example  
 [!CODE [NVC_ATL_Windowing#102](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#102)]  
  
 When a `CMyExtWindow` object receives a `WM_PAINT` message, the message is directed to `CMyExtWindow::OnPaint` for the actual processing. If `OnPaint` indicates the message requires further processing, the message will then be directed to the default message map in `CMyBaseWindow`.  
  
 In addition to the default message map, you can define an alternate message map with [ALT_MSG_MAP](../vs140/ALT_MSG_MAP.md). Always begin a message map with `BEGIN_MSG_MAP`. You can then declare subsequent alternate message maps. The following example shows the default message map and one alternate message map, each containing one handler function:  
  
 [!CODE [NVC_ATL_Windowing#98](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#98)]  
  
 The next example shows two alternate message maps. The default message map is empty.  
  
 [!CODE [NVC_ATL_Windowing#99](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#99)]  
  
 The [END_MSG_MAP](../vs140/END_MSG_MAP.md) macro marks the end of the message map. Note that there is always exactly one instance of `BEGIN_MSG_MAP` and `END_MSG_MAP`.  
  
 For more information about using message maps in ATL, see [Message Maps](../vs140/Message-Maps--ATL-.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [CMessageMap Class](../vs140/CMessageMap-Class.md)   
 [CDynamicChain Class](../vs140/CDynamicChain-Class.md)