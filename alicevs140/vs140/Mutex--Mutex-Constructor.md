---
title: "Mutex::Mutex Constructor"
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
ms.topic: reference
ms.assetid: 504afcdc-775a-4c98-a06f-4fb4663eba3f
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Mutex::Mutex Constructor
Initializes a new instance of the Mutex class.  
  
## Syntax  
  
```  
explicit Mutex(  
   HANDLE h  
);  
  
Mutex(  
   _Inout_ Mutex&& h  
);  
```  
  
#### Parameters  
 `h`  
 A handle, or an rvalue-reference to a handle, to a Mutex object.  
  
## Remarks  
 The first constructor initializes a Mutex object from the specified handle. The second constructor initializes a Mutex object from the specified handle, and then moves ownership of the mutex to the current Mutex object.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Mutex Class](../vs140/Mutex-Class.md)