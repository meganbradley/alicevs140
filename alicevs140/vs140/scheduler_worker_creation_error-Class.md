---
title: "scheduler_worker_creation_error Class"
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
ms.assetid: 4aec1c3e-c32a-41b2-899d-2d898f23b3c7
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# scheduler_worker_creation_error Class
This class describes an exception thrown because of a failure to create a worker execution context in the Concurrency Runtime.  
  
## Syntax  
  
```  
class scheduler_worker_creation_error : public scheduler_resource_allocation_error;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[scheduler_worker_creation_error::scheduler_worker_creation_error Constructor](#scheduler_worker_creation_error__scheduler_worker_creation_error_constructor)|Overloaded. Constructs a                                         `scheduler_worker_creation_error` object.|  
  
## Remarks  
 This exception is typically thrown when a call to the operating system to create execution contexts from within the Concurrency Runtime fails. Execution contexts are threads that execute tasks in the Concurrency Runtime. The error code which would normally be returned from a call to the Win32 method                 `GetLastError` is converted to a value of type                 `HRESULT` and can be retrieved using the base class method                 `get_error_code`.  
  
## Inheritance Hierarchy  
 `exception`  
  
 [scheduler_resource_allocation_error](../vs140/scheduler_resource_allocation_error-Class.md)  
  
 `scheduler_worker_creation_error`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="scheduler_worker_creation_error__scheduler_worker_creation_error_constructor"></a>  scheduler_worker_creation_error::scheduler_worker_creation_error Constructor  
 Constructs a                 `scheduler_worker_creation_error` object.  
  
```  
scheduler_worker_creation_error(  
   _In_z_ const char *                 _Message,  
   HRESULT                 _Hresult  
) throw();  
  
explicit _CRTIMP scheduler_worker_creation_error(  
   HRESULT                 _Hresult  
) throw();  
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
 `_Hresult`  
 The                                 `HRESULT` value of the error that caused the exception.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)