---
title: "invalid_operation Class"
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
ms.assetid: 26ba07dc-fcdf-44cb-b748-a31d35205b52
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_operation Class
This class describes an exception thrown when an invalid operation is performed that is not more accurately described by another exception type thrown by the Concurrency Runtime.  
  
## Syntax  
  
```  
class invalid_operation : public std::exception;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[invalid_operation::invalid_operation Constructor](#invalid_operation__invalid_operation_constructor)|Overloaded. Constructs an                                         `invalid_operation` object.|  
  
## Remarks  
 The various methods which throw this exception will generally document under what circumstances they will throw it.  
  
## Inheritance Hierarchy  
 `exception`  
  
 `invalid_operation`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="invalid_operation__invalid_operation_constructor"></a>  invalid_operation::invalid_operation Constructor  
 Constructs an                 `invalid_operation` object.  
  
```  
explicit _CRTIMP invalid_operation(  
   _In_z_ const char *                 _Message  
) throw();  
  
invalid_operation() throw();  
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)