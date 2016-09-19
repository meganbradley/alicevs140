---
title: "transformer::link_target_notification Method"
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
ms.assetid: 418227fb-f395-47cb-a297-9e030670d235
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# transformer::link_target_notification Method
A callback that notifies that a new target has been linked to this `transformer` messaging block.  
  
## Syntax  
  
```  
virtual void link_target_notification(  
   _Inout_ ITarget<_Output> *  
);  
```  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [transformer Class](../vs140/transformer-Class.md)