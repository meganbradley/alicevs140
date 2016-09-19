---
title: "choice::value Method"
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
ms.assetid: 989d89cc-e3c8-4e57-8318-d5cfda0a9756
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# choice::value Method
Gets the message whose index was selected by the `choice` messaging block.  
  
## Syntax  
  
```  
template <  
   typename _Payload_type  
>  
_Payload_type const & value();  
```  
  
#### Parameters  
 `_Payload_type`  
 The type of the message payload.  
  
## Return Value  
 The payload of the message.  
  
## Remarks  
 Because a `choice` messaging block can take inputs with different payload types, you must specify the type of the payload at the point of retrieval. You can determine the type based on the result of the `index` method.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [choice Class](../vs140/choice-Class.md)