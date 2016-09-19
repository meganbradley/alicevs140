---
title: "source_link_manager::register_target_block Method"
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
ms.assetid: 00c55cbc-4955-4549-9a8a-0c0e5022ae26
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# source_link_manager::register_target_block Method
Registers the target block that holds this `source_link_manager` object.  
  
## Syntax  
  
```  
void register_target_block(  
   _Inout_ ITarget<typename _Block::source_type> * _PTarget  
);  
```  
  
#### Parameters  
 `_PTarget`  
 The target block holding this `source_link_manager` object.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [source_link_manager Class](../vs140/source_link_manager-Class.md)