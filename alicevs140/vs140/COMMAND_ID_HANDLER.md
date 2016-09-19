---
title: "COMMAND_ID_HANDLER"
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
ms.assetid: 608e202c-6cc9-4ab1-95ad-5678262e56d7
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COMMAND_ID_HANDLER
Similar to [COMMAND_HANDLER](../vs140/COMMAND_HANDLER.md), but maps a [WM_COMMAND](http://msdn.microsoft.com/library/windows/desktop/ms647591) message based only on the identifier of the menu item, control, or accelerator.  
  
## Syntax  
  
```  
  
COMMAND_ID_HANDLER(   
id  
,   
func  
 )  
  
```  
  
#### Parameters  
 `id`  
 [in] The identifier of the menu item, control, or accelerator sending the message.  
  
 `func`  
 [in] The name of the message-handler function.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [COMMAND_CODE_HANDLER](../vs140/COMMAND_CODE_HANDLER.md)   
 [COMMAND_RANGE_HANDLER](../vs140/COMMAND_RANGE_HANDLER.md)   
 [MESSAGE_HANDLER](../vs140/MESSAGE_HANDLER.md)   
 [NOTIFY_ID_HANDLER](../vs140/NOTIFY_ID_HANDLER.md)