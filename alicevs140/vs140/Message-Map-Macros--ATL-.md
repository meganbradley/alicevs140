---
title: "Message Map Macros (ATL)"
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
ms.assetid: eefdd546-8934-4a30-b263-9c06a8addcbd
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Message Map Macros (ATL)
These macros define message maps and entries.  
  
|||  
|-|-|  
|[ALT_MSG_MAP](../vs140/ALT_MSG_MAP.md)|Marks the beginning of an alternate message map.|  
|[BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md)|Marks the beginning of the default message map.|  
|[CHAIN_MSG_MAP_ALT](../vs140/CHAIN_MSG_MAP_ALT.md)|Chains to an alternate message map in the base class.|  
|[CHAIN_MSG_MAP_ALT_MEMBER](../vs140/CHAIN_MSG_MAP_ALT_MEMBER.md)|Chains to an alternate message map in a data member of the class.|  
|[CHAIN_MSG_MAP](../vs140/CHAIN_MSG_MAP.md)|Chains to the default message map in the base class.|  
|[CHAIN_MSG_MAP_DYNAMIC](../vs140/CHAIN_MSG_MAP_DYNAMIC.md)|Chains to the message map in another class at run time.|  
|[CHAIN_MSG_MAP_MEMBER](../vs140/CHAIN_MSG_MAP_MEMBER.md)|Chains to the default message map in a data member of the class.|  
|[COMMAND_CODE_HANDLER](../vs140/COMMAND_CODE_HANDLER.md)|Maps a **WM_COMMAND** message to a handler function, based on the notification code.|  
|[COMMAND_HANDLER](../vs140/COMMAND_HANDLER.md)|Maps a **WM_COMMAND** message to a handler function, based on the notification code and the identifier of the menu item, control, or accelerator.|  
|[COMMAND_ID_HANDLER](../vs140/COMMAND_ID_HANDLER.md)|Maps a **WM_COMMAND** message to a handler function, based on the identifier of the menu item, control, or accelerator.|  
|[COMMAND_RANGE_CODE_HANDLER](../vs140/COMMAND_RANGE_CODE_HANDLER.md)|Maps a **WM_COMMAND** message to a handler function, based on the notification code and a contiguous range of control identifiers.|  
|[COMMAND_RANGE_HANDLER](../vs140/COMMAND_RANGE_HANDLER.md)|Maps a **WM_COMMAND** message to a handler function, based on a contiguous range of control identifiers.|  
|[DECLARE_EMPTY_MSG_MAP](../vs140/DECLARE_EMPTY_MSG_MAP.md)|Implements an empty message map.|  
|[DEFAULT_REFLECTION_HANDLER](../vs140/DEFAULT_REFLECTION_HANDLER.md)|Provides a default handler for reflected messages that are not handled otherwise.|  
|[END_MSG_MAP](../vs140/END_MSG_MAP.md)|Marks the end of a message map.|  
|[FORWARD_NOTIFICATIONS](../vs140/FORWARD_NOTIFICATIONS.md)|Forwards notification messages to the parent window.|  
|[MESSAGE_HANDLER](../vs140/MESSAGE_HANDLER.md)|Maps a Windows message to a handler function.|  
|[MESSAGE_RANGE_HANDLER](../vs140/MESSAGE_RANGE_HANDLER.md)|Maps a contiguous range of Windows messages to a handler function.|  
|[NOTIFY_CODE_HANDLER](../vs140/NOTIFY_CODE_HANDLER.md)|Maps a **WM_NOTIFY** message to a handler function, based on the notification code.|  
|[NOTIFY_HANDLER](../vs140/NOTIFY_HANDLER.md)|Maps a **WM_NOTIFY** message to a handler function, based on the notification code and the control identifier.|  
|[NOTIFY_ID_HANDLER](../vs140/NOTIFY_ID_HANDLER.md)|Maps a **WM_NOTIFY** message to a handler function, based on the control identifier.|  
|[NOTIFY_RANGE_CODE_HANDLER](../vs140/NOTIFY_RANGE_CODE_HANDLER.md)|Maps a **WM_NOTIFY** message to a handler function, based on the notification code and a contiguous range of control identifiers.|  
|[NOTIFY_RANGE_HANDLER](../vs140/NOTIFY_RANGE_HANDLER.md)|Maps a **WM_NOTIFY** message to a handler function, based on a contiguous range of control identifiers.|  
|[REFLECT_NOTIFICATIONS](../vs140/REFLECT_NOTIFICATIONS.md)|Reflects notification messages back to the window that sent them.|  
|[REFLECTED_COMMAND_CODE_HANDLER](../vs140/REFLECTED_COMMAND_CODE_HANDLER.md)|Maps a reflected **WM_COMMAND** message to a handler function, based on the notification code.|  
|[REFLECTED_COMMAND_HANDLER](../vs140/REFLECTED_COMMAND_HANDLER.md)|Maps a reflected **WM_COMMAND** message to a handler function, based on the notification code and the identifier of the menu item, control, or accelerator.|  
|[REFLECTED_COMMAND_ID_HANDLER](../vs140/REFLECTED_COMMAND_ID_HANDLER.md)|Maps a reflected **WM_COMMAND** message to a handler function, based on the identifier of the menu item, control, or accelerator.|  
|[REFLECTED_COMMAND_RANGE_CODE_HANDLER](../vs140/REFLECTED_COMMAND_RANGE_CODE_HANDLER.md)|Maps a reflected **WM_COMMAND** message to a handler function, based on the notification code and a contiguous range of control identifiers.|  
|[REFLECTED_COMMAND_RANGE_HANDLER](../vs140/REFLECTED_COMMAND_RANGE_HANDLER.md)|Maps a reflected **WM_COMMAND** message to a handler function, based on a contiguous range of control identifiers.|  
|[REFLECTED_NOTIFY_CODE_HANDLER](../vs140/REFLECTED_NOTIFY_CODE_HANDLER.md)|Maps a reflected **WM_NOTIFY** message to a handler function, based on the notification code.|  
|[REFLECTED_NOTIFY_HANDLER](../vs140/REFLECTED_NOTIFY_HANDLER.md)|Maps a reflected **WM_NOTIFY** message to a handler function, based on the notification code and the control identifier.|  
|[REFLECTED_NOTIFY_ID_HANDLER](../vs140/REFLECTED_NOTIFY_ID_HANDLER.md)|Maps a reflected **WM_NOTIFY** message to a handler function, based on the control identifier.|  
|[REFLECTED_NOTIFY_RANGE_CODE_HANDLER](../vs140/REFLECTED_NOTIFY_RANGE_CODE_HANDLER.md)|Maps a reflected **WM_NOTIFY** message to a handler function, based on the notification code and a contiguous range of control identifiers.|  
|[REFLECTED_NOTIFY_RANGE_HANDLER](../vs140/REFLECTED_NOTIFY_RANGE_HANDLER.md)|Maps a reflected **WM_NOTIFY** message to a handler function, based on a contiguous range of control identifiers.|  
  
## See Also  
 [Macros](../vs140/ATL-Macros.md)