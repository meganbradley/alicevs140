---
title: "improper_lock Class"
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
ms.assetid: 8f494942-7748-4a2a-8de2-23414bfe6346
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# improper_lock Class
This class describes an exception thrown when a lock is acquired improperly.  
  
## Syntax  
  
```  
class improper_lock : public std::exception;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[improper_lock::improper_lock Constructor](#improper_lock__improper_lock_constructor)|Overloaded. Constructs an                                         `improper_lock exception`.|  
  
## Remarks  
 Typically, this exception is thrown when an attempt is made to acquire a non-reentrant lock recursively on the same context.  
  
## Inheritance Hierarchy  
 `exception`  
  
 `improper_lock`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="improper_lock__improper_lock_constructor"></a>  improper_lock::improper_lock Constructor  
 Constructs an                 `improper_lock exception`.  
  
```  
explicit _CRTIMP improper_lock(  
   _In_z_ const char *                 _Message  
) throw();  
  
improper_lock() throw();  
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [critical_section Class](../vs140/critical_section-Class.md)   
 [reader_writer_lock Class](../vs140/reader_writer_lock-Class.md)