---
title: "HandleT::Detach Method"
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
ms.assetid: f7df0f90-fafb-4d1b-a215-a6c62941f6b0
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HandleT::Detach Method
Disassociates the current HandleT object from its underlying handle.  
  
## Syntax  
  
```  
typename HandleTraits::Type Detach();  
```  
  
## Return Value  
 The underlying handle.  
  
## Remarks  
 When this operation completes, the current HandleT is set to the invalid state.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [HandleT Class](../vs140/HandleT-Class.md)