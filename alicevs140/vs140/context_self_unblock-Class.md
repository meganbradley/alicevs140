---
title: "context_self_unblock Class"
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
ms.assetid: 9601cd28-4f40-4c2e-89ab-747068956331
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# context_self_unblock Class
This class describes an exception thrown when the             `Unblock` method of a             `Context` object is called from the same context. This would indicate an attempt by a given context to unblock itself.  
  
## Syntax  
  
```  
class context_self_unblock : public std::exception;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[context_self_unblock::context_self_unblock Constructor](#context_self_unblock__context_self_unblock_constructor)|Overloaded. Constructs a                                         `context_self_unblock` object.|  
  
## Inheritance Hierarchy  
 `exception`  
  
 `context_self_unblock`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="context_self_unblock__context_self_unblock_constructor"></a>  context_self_unblock::context_self_unblock Constructor  
 Constructs a                 `context_self_unblock` object.  
  
```  
explicit _CRTIMP context_self_unblock(  
   _In_z_ const char *                 _Message  
) throw();  
  
context_self_unblock() throw();  
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [Context Class](../vs140/Context-Class.md)   
 [Context::Unblock Method](../vs140/Context-Class.md#context__unblock_method)