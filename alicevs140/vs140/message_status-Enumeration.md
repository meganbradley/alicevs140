---
title: "message_status Enumeration"
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
ms.topic: article
ms.assetid: e5e05af0-734d-4063-ae32-f6356382f313
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# message_status Enumeration
The valid responses for an offer of a `message` object to a block.  
  
## Syntax  
  
```  
enum message_status;  
```  
  
## Members  
  
### Values  
  
|Name|Description|  
|----------|-----------------|  
|`accepted`|The target accepted the message.|  
|`declined`|The target did not accept the message.|  
|`missed`|The target tried to accept the message, but it was no longer available.|  
|`postponed`|The target postponed the message.|  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)