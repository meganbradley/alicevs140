---
title: "DispatchState::m_fIsPreviousContextAsynchronouslyBlocked Data Member"
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
ms.assetid: 386ec117-c630-4278-ba30-be4b39e13a79
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DispatchState::m_fIsPreviousContextAsynchronouslyBlocked Data Member
Tells whether this context has entered the `Dispatch` method because the previous context asynchronously blocked. This is used only on the UMS scheduling context, and is set to the value `0` for all other execution contexts.  
  
## Syntax  
  
```  
unsigned int m_fIsPreviousContextAsynchronouslyBlocked : 1;  
```  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [DispatchState Structure](../vs140/DispatchState-Structure.md)   
 [IExecutionContext::Dispatch Method](../vs140/IExecutionContext--Dispatch-Method.md)