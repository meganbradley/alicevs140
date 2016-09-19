---
title: "asend Function"
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
ms.assetid: 920dc665-7e23-4bd7-8c74-3e74067aa52a
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# asend Function
An asynchronous send operation, which schedules a task to propagate the data to the target block.  
  
## Syntax  
  
```  
template <  
   class _Type  
>  
bool asend(  
   _Inout_ ITarget<_Type> * _Trg,  
   const _Type& _Data  
);  
  
template <  
   class _Type  
>  
bool asend(  
   ITarget<_Type> &_Trg,  
   const _Type &_Data  
);  
```  
  
#### Parameters  
 `_Type`  
 The type of the data to be sent.  
  
 `_Trg`  
 A pointer or reference to the target to which data is sent.  
  
 `_Data`  
 A reference to the data to be sent.  
  
## Return Value  
 `true` if the message was accepted before the method returned, `false` otherwise.  
  
## Remarks  
 For more information, see [Message Passing Functions](../vs140/Message-Passing-Functions.md).  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [receive Function](../vs140/receive-Function.md)   
 [try_receive Function](../vs140/try_receive-Function.md)   
 [send Function](../vs140/send-Function.md)