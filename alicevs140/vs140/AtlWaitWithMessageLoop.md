---
title: "AtlWaitWithMessageLoop"
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
ms.assetid: df79fd70-c33e-41e7-b340-f68278e28322
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlWaitWithMessageLoop
Waits for the object to be signaled, meanwhile dispatching window messages as needed.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      BOOL AtlWaitWithMessageLoop(  
HANDLE hEvent   
);  
```  
  
#### Parameters  
 `hEvent`  
 [in] The handle of the object to wait for.  
  
## Return Value  
 Returns **TRUE** if the object has been signaled.  
  
## Remarks  
 This is useful if you want to wait for an object's event to happen and be notified of it happening, but allow window messages to be dispatched while waiting.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Event Handling Global Functions](../vs140/Event-Handling-Global-Functions.md)