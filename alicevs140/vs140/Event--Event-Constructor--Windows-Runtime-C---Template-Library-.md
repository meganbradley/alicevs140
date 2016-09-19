---
title: "Event::Event Constructor (Windows Runtime C++ Template Library)"
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
ms.assetid: 21495297-9612-4095-9256-16e168cc0021
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event::Event Constructor (Windows Runtime C++ Template Library)
Initializes a new instance of the Event class.  
  
## Syntax  
  
```  
explicit Event(  
   HANDLE h = HandleT::Traits::GetInvalidValue()  
);  
WRL_NOTHROW Event(  
   _Inout_ Event&& h  
);  
```  
  
#### Parameters  
 `h`  
 Handle to an event. By default, `h` is initialized to `nullptr`.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Event Class](../vs140/Event-Class--Windows-Runtime-C---Template-Library-.md)