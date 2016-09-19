---
title: "_callnewh"
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
apiname: 
  - _callnewh
apilocation: 
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 4dcb73e9-6384-4d12-a973-a8807d4de7a8
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _callnewh
Calls the currently installed *new handler*.  
  
## Syntax  
  
```cpp  
int _callnewh(  
   size_t size  
   )  
```  
  
#### Parameters  
 `size`  
 The amount of memory that the [new operator](../vs140/new-Operator--C---.md) tried to allocate.  
  
## Return Value  
  
|Value|Description|  
|-----------|-----------------|  
|0|Failure: Either no new handler is installed or no new handler is active.|  
|1|Success: The new handler is installed and active. The memory allocation can be retried.|  
  
## Exceptions  
 This function throws [bad_alloc](../vs140/bad_alloc-Class.md) if the *new handler* can’t be located.  
  
## Remarks  
 The *new handler* is called if the [new operator](../vs140/new-Operator--C---.md) fails to successfully allocate memory. The new handler might then initiate some appropriate action, such as freeing memory so that subsequent allocations succeed.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|_callnewh|internal.h|  
  
## See Also  
 [_set_new_handler](../vs140/_set_new_handler.md)   
 [_set_new_mode](../vs140/_set_new_mode.md)