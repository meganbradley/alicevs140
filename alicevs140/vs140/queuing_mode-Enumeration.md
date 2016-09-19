---
title: "queuing_mode Enumeration"
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
ms.assetid: 8c641054-906d-40b3-bbb4-f62af9356a14
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# queuing_mode Enumeration
Specifies the queuing modes that are supported on the accelerator.  
  
## Syntax  
  
```  
enum queuing_mode;  
```  
  
## Members  
  
### Values  
  
|Name|Description|  
|----------|-----------------|  
|`queuing_mode_immediate`|A queuing mode that specifies that any commands, for example, [parallel_for_each Function (C++ AMP)](../vs140/parallel_for_each-Function--C---AMP-.md), are sent to the corresponding accelerator device as soon as they return to the caller.|  
|`queuing_mode_automatic`|A queuing mode that specifies that commands be queued up on a command queue that corresponds to the [accelerator_view](../vs140/accelerator_view-Class.md) object. Commands are sent to the device when [accelerator_view::flush](../vs140/accelerator_view--flush-Method.md) is called.|  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [Concurrency Namespace](../vs140/Concurrency-Namespace--C---AMP-.md)