---
title: "target_block::wait_for_async_sends Method"
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
ms.assetid: 2d890e3f-aeb6-43de-afc4-ebfbbf556ec7
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# target_block::wait_for_async_sends Method
Waits for all asynchronous propagations to complete.  
  
## Syntax  
  
```  
void wait_for_async_sends();  
```  
  
## Remarks  
 This method is used by message block destructors to ensure all asynchronous operations have had time to finish before destroying the block.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [target_block Class](../vs140/target_block-Class.md)