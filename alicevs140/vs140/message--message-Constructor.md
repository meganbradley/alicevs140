---
title: "message::message Constructor"
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
ms.assetid: 515d2743-1a79-479f-bd84-e3fc49faa607
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# message::message Constructor
Constructs a `message` object.  
  
## Syntax  
  
```  
message(  
   _Type const &_P  
);  
  
message(  
   _Type const &_P,  
   runtime_object_identity _Id  
);  
  
message(  
   message const & _Msg  
);  
  
message(  
   _In_ message const * _Msg  
);  
```  
  
#### Parameters  
 `_P`  
 The payload of this message.  
  
 `_Id`  
 The unique ID of this message.  
  
 `_Msg`  
 A reference or pointer to a `message` object.  
  
## Remarks  
 The constructor that takes a pointer to a `message` object as an argument throws an [invalid_argument](../vs140/invalid_argument-Class.md) exception if the parameter `_Msg` is `NULL`.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [message Class](../vs140/message-Class.md)