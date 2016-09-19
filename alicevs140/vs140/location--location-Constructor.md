---
title: "location::location Constructor"
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
ms.assetid: 77cc1871-3f22-4311-923f-b55fe0041f21
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# location::location Constructor
Constructs a `location` object.  
  
## Syntax  
  
```  
location();  
  
location(  
   const location& _Src  
);  
  
location(  
   _Type _LocationType,  
   unsigned int _Id,  
   unsigned int _BindingId = 0,  
   _Inout_opt_ void *_PBinding = NULL  
);  
```  
  
#### Parameters  
 `_Src`  
 `_LocationType`  
 `_Id`  
 `_BindingId`  
 `_PBinding`  
  
## Remarks  
 A default constructed location represents the system as a whole.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [location Class](../vs140/location-Class.md)