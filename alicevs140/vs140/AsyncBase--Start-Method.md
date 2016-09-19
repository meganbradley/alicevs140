---
title: "AsyncBase::Start Method"
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
ms.assetid: 67405c9d-0d1a-4c1e-8ea4-6ba01c1f90d9
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AsyncBase::Start Method
Starts the asynchronous operation.  
  
## Syntax  
  
```  
STDMETHOD(  
   Start  
)(void);  
```  
  
## Return Value  
 S_OK if the operation starts or is already started; otherwise, E_ILLEGAL_STATE_CHANGE.  
  
## Remarks  
 Start() is a default implementation of IAsyncInfo::Start, and does no actual work. To actually start an asynchronous operation, override the OnStart() pure virtual method.  
  
## Requirements  
 **Header:** async.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [AsyncBase Class](../vs140/AsyncBase-Class.md)