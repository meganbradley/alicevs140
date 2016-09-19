---
title: "single_assignment::link_target_notification Method"
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
ms.assetid: 8fbcab33-7fe1-4df0-a362-e9a833ede4a1
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# single_assignment::link_target_notification Method
A callback that notifies that a new target has been linked to this `single_assignment` messaging block.  
  
## Syntax  
  
```  
virtual void link_target_notification(  
   _Inout_ ITarget<_Type> * _PTarget  
);  
```  
  
#### Parameters  
 `_PTarget`  
 A pointer to the newly linked target.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [single_assignment Class](../vs140/single_assignment-Class.md)