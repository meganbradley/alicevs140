---
title: "ios_base::event_callback"
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
ms.assetid: ab1e565e-32e9-49a9-845a-1a9f28f6e042
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ios_base::event_callback
Describes a function passed to [register_call](../vs140/ios_base--register_callback.md).  
  
## Syntax  
  
```  
  
      typedef void (  
      __  
      cdecl *event  
      _  
      callback)(  
   event _E,  
   ios_base& _Base,  
   int _I  
);  
```  
  
#### Parameters  
 *_E*  
 The [event](../vs140/ios_base--event.md).  
  
 `_Base`  
 The stream in which the event was called.  
  
 *_I*  
 A user-defined number.  
  
## Remarks  
 The type describes a pointer to a function that can be registered with [register_callback](../vs140/ios_base--register_callback.md). This type of function must not throw an exception.  
  
## Example  
 See [register_call](../vs140/ios_base--register_callback.md) for an example that uses `event_callback`.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [ios_base Class](../vs140/ios_base-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)