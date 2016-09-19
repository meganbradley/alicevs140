---
title: "NOTIFY_RANGE_HANDLER"
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
ms.assetid: 9a3896fb-8faf-4f17-9184-dda88725f943
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NOTIFY_RANGE_HANDLER
Similar to [NOTIFY_HANDLER](../vs140/NOTIFY_HANDLER.md), but maps [WM_NOTIFY](http://msdn.microsoft.com/library/windows/desktop/bb775583) messages from a range of controls to a single handler function.  
  
## Syntax  
  
```  
  
      NOTIFY_RANGE_HANDLER(   
   idFirst,   
   idLast,   
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
 This range is based on the identifier of the control sending the message.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [NOTIFY_ID_HANDLER](../vs140/NOTIFY_ID_HANDLER.md)   
 [NOTIFY_CODE_HANDLER](../vs140/NOTIFY_CODE_HANDLER.md)   
 [REFLECTED_NOTIFY_CODE_HANDLER](../vs140/REFLECTED_NOTIFY_CODE_HANDLER.md)   
 [COMMAND_RANGE_CODE_HANDLER](../vs140/COMMAND_RANGE_CODE_HANDLER.md)   
 [MESSAGE_RANGE_HANDLER](../vs140/MESSAGE_RANGE_HANDLER.md)