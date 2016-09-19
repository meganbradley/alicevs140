---
title: "REFLECTED_COMMAND_RANGE_HANDLER"
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
ms.assetid: d38030b1-54d9-4e55-a006-c3c23a793592
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# REFLECTED_COMMAND_RANGE_HANDLER
Similar to [COMMAND_RANGE_HANDLER](../vs140/COMMAND_RANGE_HANDLER.md), but maps commands reflected from the parent window.  
  
## Syntax  
  
```  
  
      REFLECTED_COMMAND_RANGE_HANDLER(   
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
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [REFLECT_NOTIFICATIONS](../vs140/REFLECT_NOTIFICATIONS.md)