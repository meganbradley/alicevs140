---
title: "invalid_multiple_scheduling Class"
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
ms.assetid: e9a47cb7-a778-4df7-92b0-3752119fd4c7
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_multiple_scheduling Class
This class describes an exception thrown when a             `task_handle` object is scheduled multiple times using the             `run` method of a             `task_group` or             `structured_task_group` object without an intervening call to either the             `wait` or             `run_and_wait` methods.  
  
## Syntax  
  
```  
class invalid_multiple_scheduling : public std::exception;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[invalid_multiple_scheduling::invalid_multiple_scheduling Constructor](#invalid_multiple_scheduling__invalid_multiple_scheduling_constructor)|Overloaded. Constructs an                                         `invalid_multiple_scheduling` object.|  
  
## Inheritance Hierarchy  
 `exception`  
  
 `invalid_multiple_scheduling`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="invalid_multiple_scheduling__invalid_multiple_scheduling_constructor"></a>  invalid_multiple_scheduling::invalid_multiple_scheduling Constructor  
 Constructs an                 `invalid_multiple_scheduling` object.  
  
```  
explicit _CRTIMP invalid_multiple_scheduling(  
   _In_z_ const char *                 _Message  
) throw();  
  
invalid_multiple_scheduling() throw();  
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [task_handle Class](../vs140/task_handle-Class.md)   
 [task_group Class](../vs140/task_group-Class.md)   
 [task_group::run Method](../vs140/task_group-Class.md#task_group__run_method)   
 [task_group::wait Method](../vs140/task_group-Class.md#task_group__wait_method)   
 [task_group::run_and_wait Method](../vs140/task_group-Class.md#task_group__run_and_wait_method)   
 [structured_task_group Class](../vs140/structured_task_group-Class.md)   
 [structured_task_group::run Method](../vs140/structured_task_group-Class.md#structured_task_group__run_method)   
 [structured_task_group::wait Method](../vs140/structured_task_group-Class.md#structured_task_group__wait_method)   
 [structured_task_group::run_and_wait Method](../vs140/structured_task_group-Class.md#structured_task_group__run_and_wait_method)