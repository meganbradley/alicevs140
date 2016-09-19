---
title: "REFLECTED_COMMAND_HANDLER"
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
ms.assetid: c13aff85-1ca6-4523-95b0-12c9c71faaa0
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# REFLECTED_COMMAND_HANDLER
Similar to [COMMAND_HANDLER](../vs140/COMMAND_HANDLER.md), but maps commands reflected from the parent window.  
  
## Syntax  
  
```  
  
      REFLECTED_COMMAND_HANDLER(   
   id,   
   code,   
   func    
)  
```  
  
#### Parameters  
 `id`  
 [in] The identifier of the menu item, control, or accelerator.  
  
 `code`  
 [in] The notification code.  
  
 `func`  
 [in] The name of the message-handler function.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [REFLECT_NOTIFICATIONS](../vs140/REFLECT_NOTIFICATIONS.md)