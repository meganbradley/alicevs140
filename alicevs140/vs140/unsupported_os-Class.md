---
title: "unsupported_os Class"
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
ms.assetid: 6fa57636-341b-4b51-84cc-261d283ff736
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unsupported_os Class
This class describes an exception thrown when an unsupported operating system is used.  
  
## Syntax  
  
```  
class unsupported_os : public std::exception;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[unsupported_os::unsupported_os Constructor](#unsupported_os__unsupported_os_constructor)|Overloaded. Constructs an                                         `unsupported_os` object.|  
  
## Inheritance Hierarchy  
 `exception`  
  
 `unsupported_os`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="unsupported_os__unsupported_os_constructor"></a>  unsupported_os::unsupported_os Constructor  
 Constructs an                 `unsupported_os` object.  
  
```  
explicit _CRTIMP unsupported_os(  
   _In_z_ const char *                 _Message  
) throw();  
  
unsupported_os() throw();  
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)