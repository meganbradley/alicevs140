---
title: "MESSAGE_RANGE_HANDLER"
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
ms.assetid: a8def99f-246d-497e-8749-0977cbf1934e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MESSAGE_RANGE_HANDLER
Similar to [MESSAGE_HANDLER](../vs140/MESSAGE_HANDLER.md), but maps a range of Windows messages to a single handler function.  
  
## Syntax  
  
```  
  
      MESSAGE_RANGE_HANDLER(   
   msgFirst,   
   msgLast,   
   func    
)  
```  
  
#### Parameters  
 *msgFirst*  
 [in] Marks the beginning of a contiguous range of messages.  
  
 *msgLast*  
 [in] Marks the end of a contiguous range of messages.  
  
 `func`  
 [in] The name of the message-handler function.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [COMMAND_RANGE_HANDLER](../vs140/COMMAND_RANGE_HANDLER.md)   
 [NOTIFY_RANGE_HANDLER](../vs140/NOTIFY_RANGE_HANDLER.md)