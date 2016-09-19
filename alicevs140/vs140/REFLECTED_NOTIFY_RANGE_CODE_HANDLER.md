---
title: "REFLECTED_NOTIFY_RANGE_CODE_HANDLER"
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
ms.assetid: f2dcd90d-fcd1-4031-9c4b-845889acc816
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# REFLECTED_NOTIFY_RANGE_CODE_HANDLER
Similar to [NOTIFY_RANGE_CODE_HANDLER](../vs140/NOTIFY_RANGE_CODE_HANDLER.md), but maps notifications reflected from the parent window.  
  
## Syntax  
  
```  
  
      REFLECTED_NOTIFY_RANGE_CODE_HANDLER(  
   idFirst,   
   idLast,    
   cd,    
   func  
)  
```  
  
#### Parameters  
 `idFirst`  
 [in] Marks the beginning of a contiguous range of control identifiers.  
  
 `idLast`  
 [in] Marks the end of a contiguous range of control identifiers.  
  
 `cd`  
 [in] The notification code.  
  
 `func`  
 [in] The name of the message-handler function.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [REFLECT_NOTIFICATIONS](../vs140/REFLECT_NOTIFICATIONS.md)