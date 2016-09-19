---
title: "access_type Enumeration"
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
ms.assetid: a1b2d084-38dd-4fb6-b268-48e3ab15d634
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# access_type Enumeration
Enumeration type used to denote the various types of access to data.  
  
## Syntax  
  
```  
enum access_type;  
```  
  
## Members  
  
### Values  
  
|Name|Description|  
|----------|-----------------|  
|`access_type_auto`|Automatically choose the best `access_type` for the accelerator.|  
|`access_type_none`|Dedicated. The allocation is only accessible on the accelerator and not on the CPU.|  
|`access_type_read`|Shared. The allocation is accessible on the accelerator and is readable on the CPU.|  
|`access_type_read_write`|Shared. The allocation is accessible on the accelerator and is writable on the CPU.|  
|`access_type_write`|Shared. The allocation is accessible on the accelerator and is both readable and writable on the CPU.|  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace (C++ AMP)](../vs140/Concurrency-Namespace--C---AMP-.md)