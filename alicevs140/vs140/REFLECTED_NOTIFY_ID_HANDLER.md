---
title: "REFLECTED_NOTIFY_ID_HANDLER"
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
ms.assetid: 06554d4b-b66a-4deb-9fa0-201f2d5219f3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# REFLECTED_NOTIFY_ID_HANDLER
Similar to [NOTIFY_ID_HANDLER](../vs140/NOTIFY_ID_HANDLER.md), but maps notifications reflected from the parent window.  
  
## Syntax  
  
```  
  
      REFLECTED_NOTIFY_ID_HANDLER(   
   id,   
   func    
)  
```  
  
#### Parameters  
 `id`  
 [in] The identifier of the menu item, control, or accelerator.  
  
 `func`  
 [in] The name of the message-handler function.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [REFLECT_NOTIFICATIONS](../vs140/REFLECT_NOTIFICATIONS.md)