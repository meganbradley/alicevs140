---
title: "AsyncBase::TryTransitionToCompleted Method"
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
ms.assetid: 8d038e0a-47ec-4cfc-8aeb-6821282df67a
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AsyncBase::TryTransitionToCompleted Method
Indicates whether the current asynchronous operation has completed.  
  
## Syntax  
  
```  
bool TryTransitionToCompleted(  
   void  
);  
```  
  
## Return Value  
 `true` if the asynchronous operation has completed; otherwise, `false`.  
  
## Requirements  
 **Header:** async.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [AsyncBase Class](../vs140/AsyncBase-Class.md)