---
title: "HandleT::HandleT Constructor"
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
ms.assetid: 4def6891-7e53-46f1-a197-a80e10744dd5
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HandleT::HandleT Constructor
Initializes a new instance of the HandleT class.  
  
## Syntax  
  
```  
explicit HandleT(  
   typename HandleTraits::Type h =   
      HandleTraits::GetInvalidValue()  
);  
  
HandleT(  
   _Inout_ HandleT&& h  
);  
```  
  
#### Parameters  
 `h`  
 A handle.  
  
## Remarks  
 The first constructor initializes a HandleT object that is not a valid handle to an object. The second constructor creates a new HandleT object from parameter `h`.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [HandleT Class](../vs140/HandleT-Class.md)