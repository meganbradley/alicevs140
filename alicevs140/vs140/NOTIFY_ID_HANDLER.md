---
title: "NOTIFY_ID_HANDLER"
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
ms.assetid: 1fd8bd36-c368-4d69-8743-15e9f12b0928
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NOTIFY_ID_HANDLER
Similar to [NOTIFY_HANDLER](../vs140/NOTIFY_HANDLER.md), but maps a [WM_NOTIFY](http://msdn.microsoft.com/library/windows/desktop/bb775583) message based only on the control identifier.  
  
## Syntax  
  
```  
  
      NOTIFY_ID_HANDLER(   
   id,   
   func    
)  
```  
  
#### Parameters  
 `id`  
 [in] The identifier of the control sending the message.  
  
 `func`  
 [in] The name of the message-handler function.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [NOTIFY_CODE_HANDLER](../vs140/NOTIFY_CODE_HANDLER.md)   
 [NOTIFY_RANGE_HANDLER](../vs140/NOTIFY_RANGE_HANDLER.md)   
 [COMMAND_ID_HANDLER](../vs140/COMMAND_ID_HANDLER.md)   
 [MESSAGE_HANDLER](../vs140/MESSAGE_HANDLER.md)