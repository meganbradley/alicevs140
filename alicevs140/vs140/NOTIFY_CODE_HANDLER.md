---
title: "NOTIFY_CODE_HANDLER"
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
ms.assetid: 27fba5ac-b38a-4d50-bf51-ddaadb2bddad
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NOTIFY_CODE_HANDLER
Similar to [NOTIFY_HANDLER](../vs140/NOTIFY_HANDLER.md), but maps a [WM_NOTIFY](http://msdn.microsoft.com/library/windows/desktop/bb775583) message based only on the notification code.  
  
## Syntax  
  
```  
  
      NOTIFY_CODE_HANDLER(   
   cd,   
   func    
)  
```  
  
#### Parameters  
 `cd`  
 [in] The notification code.  
  
 `func`  
 [in] The name of the message-handler function.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [NOTIFY_ID_HANDLER](../vs140/NOTIFY_ID_HANDLER.md)   
 [REFLECTED_NOTIFY_CODE_HANDLER](../vs140/REFLECTED_NOTIFY_CODE_HANDLER.md)   
 [NOTIFY_RANGE_HANDLER](../vs140/NOTIFY_RANGE_HANDLER.md)   
 [COMMAND_CODE_HANDLER](../vs140/COMMAND_CODE_HANDLER.md)   
 [MESSAGE_HANDLER](../vs140/MESSAGE_HANDLER.md)