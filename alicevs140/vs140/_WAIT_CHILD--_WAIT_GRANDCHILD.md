---
title: "_WAIT_CHILD, _WAIT_GRANDCHILD"
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
ms.assetid: 7acd96fa-d118-4339-bb00-e5afaf286945
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _WAIT_CHILD, _WAIT_GRANDCHILD
## Syntax  
  
```  
  
#include <process.h>  
  
```  
  
## Remarks  
 The `_cwait` function can be used by any process to wait for any other process (if the process ID is known). The action argument can be one of the following values:  
  
|Constant|Meaning|  
|--------------|-------------|  
|`_WAIT_CHILD`|Calling process waits until specified new process terminates.|  
|`_WAIT_GRANDCHILD`|Calling process waits until specified new process, and all processes created by that new process, terminate.|  
  
## See Also  
 [_cwait](../vs140/_cwait.md)   
 [Global Constants](../vs140/Global-Constants.md)