---
title: "send Function"
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
ms.assetid: 8713fb36-066b-47de-af12-589fa74805d6
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# send Function
A synchronous send operation, which waits until the target either accepts or declines the message.  
  
## Syntax  
  
```  
template <  
   class _Type  
>  
bool send(  
   _Inout_ ITarget<_Type> * _Trg,  
   const _Type& _Data  
);  
  
template <  
   class _Type  
>  
bool send(  
   ITarget<_Type> &_Trg,  
   const _Type &_Data  
);  
```  
  
#### Parameters  
 `_Type`  
 The payload type.  
  
 `_Trg`  
 A pointer or reference to the target to which data is sent.  
  
 `_Data`  
 A reference to the data to be sent.  
  
## Return Value  
 `true` if the message was accepted, `false` otherwise.  
  
## Remarks  
 For more information, see [Message Passing Functions](../vs140/Message-Passing-Functions.md).  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [receive Function](../vs140/receive-Function.md)   
 [try_receive Function](../vs140/try_receive-Function.md)   
 [asend Function](../vs140/asend-Function.md)