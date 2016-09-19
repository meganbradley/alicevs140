---
title: "scheduler_not_attached Class"
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
ms.assetid: 26001970-b400-463b-be3d-8623359c399a
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# scheduler_not_attached Class
This class describes an exception thrown when an operation is performed which requires a scheduler to be attached to the current context and one is not.  
  
## Syntax  
  
```  
class scheduler_not_attached : public std::exception;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[scheduler_not_attached::scheduler_not_attached Constructor](#scheduler_not_attached__scheduler_not_attached_constructor)|Overloaded. Constructs a                                         `scheduler_not_attached` object.|  
  
## Inheritance Hierarchy  
 `exception`  
  
 `scheduler_not_attached`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="scheduler_not_attached__scheduler_not_attached_constructor"></a>  scheduler_not_attached::scheduler_not_attached Constructor  
 Constructs a                 `scheduler_not_attached` object.  
  
```  
explicit _CRTIMP scheduler_not_attached(  
   _In_z_ const char *                 _Message  
) throw();  
  
scheduler_not_attached() throw();  
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [Scheduler Class](../vs140/Scheduler-Class.md)   
 [Scheduler::Attach Method](../vs140/Scheduler-Class.md#scheduler__attach_method)