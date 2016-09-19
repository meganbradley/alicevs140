---
title: "target_block::sync_send Method"
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
ms.assetid: 83e9d689-1fa9-451d-9cb5-ff447194fe27
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# target_block::sync_send Method
Synchronously send a message for processing.  
  
## Syntax  
  
```  
void sync_send(  
   _Inout_opt_ message<_Source_type> * _PMessage  
);  
```  
  
#### Parameters  
 `_PMessage`  
 A pointer to the message being sent.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [target_block Class](../vs140/target_block-Class.md)