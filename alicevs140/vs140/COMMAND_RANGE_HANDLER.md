---
title: "COMMAND_RANGE_HANDLER"
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
ms.assetid: 5a2ba0d3-9c70-4c52-a5ae-2e7580944af7
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COMMAND_RANGE_HANDLER
Similar to [COMMAND_HANDLER](../vs140/COMMAND_HANDLER.md), but maps [WM_COMMAND](http://msdn.microsoft.com/library/windows/desktop/ms647591) messages from a range of controls to a single handler function.  
  
## Syntax  
  
```  
  
COMMAND_RANGE_HANDLER(   
idFirst  
,   
idLast  
,   
func  
 )  
  
```  
  
#### Parameters  
 `idFirst`  
 [in] Marks the beginning of a contiguous range of control identifiers.  
  
 `idLast`  
 [in] Marks the end of a contiguous range of control identifiers.  
  
 `func`  
 [in] The name of the message-handler function.  
  
## Remarks  
 This range is based on the identifier of the menu item, control, or accelerator sending the message.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [COMMAND_ID_HANDLER](../vs140/COMMAND_ID_HANDLER.md)   
 [COMMAND_CODE_HANDLER](../vs140/COMMAND_CODE_HANDLER.md)   
 [MESSAGE_RANGE_HANDLER](../vs140/MESSAGE_RANGE_HANDLER.md)   
 [NOTIFY_RANGE_HANDLER](../vs140/NOTIFY_RANGE_HANDLER.md)