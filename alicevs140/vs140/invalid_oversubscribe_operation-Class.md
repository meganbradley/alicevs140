---
title: "invalid_oversubscribe_operation Class"
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
ms.assetid: 0a9c5f08-d5e6-4ad0-90a9-517472b3ac28
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_oversubscribe_operation Class
This class describes an exception thrown when the             `Context::Oversubscribe` method is called with the             `_BeginOversubscription` parameter set to             `false` without a prior call to the             `Context::Oversubscribe` method with the             `_BeginOversubscription` parameter set to             `true`.  
  
## Syntax  
  
```  
class invalid_oversubscribe_operation : public std::exception;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[invalid_oversubscribe_operation::invalid_oversubscribe_operation Constructor](#invalid_oversubscribe_operation__invalid_oversubscribe_operation_constructor)|Overloaded. Constructs an                                         `invalid_oversubscribe_operation` object.|  
  
## Inheritance Hierarchy  
 `exception`  
  
 `invalid_oversubscribe_operation`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="invalid_oversubscribe_operation__invalid_oversubscribe_operation_constructor"></a>  invalid_oversubscribe_operation::invalid_oversubscribe_operation Constructor  
 Constructs an                 `invalid_oversubscribe_operation` object.  
  
```  
explicit _CRTIMP invalid_oversubscribe_operation(  
   _In_z_ const char *                 _Message  
) throw();  
  
invalid_oversubscribe_operation() throw();  
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [Context::Oversubscribe Method](../vs140/Context-Class.md#context__oversubscribe_method)