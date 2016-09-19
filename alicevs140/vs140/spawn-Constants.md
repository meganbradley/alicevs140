---
title: "spawn Constants"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e0533e88-d362-46fc-b53c-5f193226d879
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# spawn Constants
## Syntax  
  
```  
#include <process.h>  
```  
  
## Remarks  
 The `mode` argument determines the action taken by the calling process before and during a spawn operation. The following values for `mode` are possible:  
  
|Constant|Meaning|  
|--------------|-------------|  
|`_P_OVERLAY`|Overlays calling process with new process, destroying calling process (same effect as `_exec` calls).|  
|`_P_WAIT`|Suspends calling thread until execution of new process is complete (synchronous `_spawn`).|  
|`_P_NOWAIT`, `_P_NOWAITO`|Continues to execute calling process concurrently with new process (asynchronous `_spawn`).|  
|`_P_DETACH`|Continues to execute calling process; new process is run in background with no access to console or keyboard. Calls to `_cwait` against new process will fail. This is an asynchronous `_spawn`.|  
  
## See Also  
 [_spawn, _wspawn Functions](../vs140/_spawn--_wspawn-Functions.md)   
 [Global Constants](../vs140/Global-Constants.md)