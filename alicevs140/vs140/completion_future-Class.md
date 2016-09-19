---
title: "completion_future Class"
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
ms.assetid: 1303c62e-546d-4b02-a578-251ed3fc0b6b
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# completion_future Class
Represents a future corresponding to a C++ AMP asynchronous operation.  
  
## Syntax  
  
```  
class completion_future;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[completion_future::completion_future Constructor](../vs140/completion_future--completion_future-Constructor.md)|Initializes a new instance of the `completion_future` class.|  
|[completion_future::~completion_future Destructor](../vs140/completion_future--~completion_future-Destructor.md)|Destroys the `completion_future` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[completion_future::get Method](../vs140/completion_future--get-Method.md)|Waits until the associated asynchronous operation completes.|  
|[completion_future::then Method](../vs140/completion_future--then-Method.md)|Chains a callback function object to the `completion_future` object to be executed when the associated asynchronous operation finishes execution.|  
|[completion_future::to_task Method](../vs140/completion_future--to_task-Method.md)|Returns a `task` object corresponding to the associated asynchronous operation.|  
|[completion_future::valid Method](../vs140/completion_future--valid-Method.md)|Gets a Boolean value that indicates whether the object is associated with an asynchronous operation.|  
|[completion_future::wait Method](../vs140/completion_future--wait-Method.md)|Blocks until the associated asynchronous operation completes.|  
|[completion_future::wait_for Method](../vs140/completion_future--wait_for-Method.md)|Blocks until the associated asynchronous operation completes or the time specified by `_Rel_time` has elapsed.|  
|[completion_future::wait_until Method](../vs140/completion_future--wait_until-Method.md)|Blocks until the associated asynchronous operation completes or until the current time exceeds the value specified by `_Abs_time`.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[completion_future::operator std::shared_future<void\> Operator](../vs140/completion_future--operator-std--shared_future-void--Operator.md)|Implicitly converts the `completion_future` object to an `std::shared_future` object.|  
|[completion_future::operator= Operator](../vs140/completion_future--operator=-Operator.md)|Copies the contents of the specified `completion_future` object into this one.|  
  
## Inheritance Hierarchy  
 `completion_future`  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace (C++ AMP)](../vs140/Concurrency-Namespace--C---AMP-.md)