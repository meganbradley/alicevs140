---
title: "invalid_link_target Class"
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
ms.assetid: 33b64885-34d8-4d4e-a893-02e9f19c958e
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_link_target Class
This class describes an exception thrown when the             `link_target` method of a messaging block is called and the messaging block is unable to link to the target. This can be the result of exceeding the number of links the messaging block is allowed or attempting to link a specific target twice to the same source.  
  
## Syntax  
  
```  
class invalid_link_target : public std::exception;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[invalid_link_target::invalid_link_target Constructor](#invalid_link_target__invalid_link_target_constructor)|Overloaded. Constructs an                                         `invalid_link_target` object.|  
  
## Inheritance Hierarchy  
 `exception`  
  
 `invalid_link_target`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="invalid_link_target__invalid_link_target_constructor"></a>  invalid_link_target::invalid_link_target Constructor  
 Constructs an                 `invalid_link_target` object.  
  
```  
explicit _CRTIMP invalid_link_target(  
   _In_z_ const char *                 _Message  
) throw();  
  
invalid_link_target() throw();  
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [Asynchronous Message Blocks](../vs140/Asynchronous-Message-Blocks.md)