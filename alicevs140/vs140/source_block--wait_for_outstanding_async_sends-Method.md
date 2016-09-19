---
title: "source_block::wait_for_outstanding_async_sends Method"
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
ms.assetid: 1f8ca2c1-e2bb-4318-b569-2eafa6fb7a27
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# source_block::wait_for_outstanding_async_sends Method
Waits for all asynchronous propagations to complete. This propagator-specific spin wait is used in destructors of message blocks to make sure that all asynchronous propagations have time to finish before destroying the block.  
  
## Syntax  
  
```  
void wait_for_outstanding_async_sends();  
```  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [source_block Class](../vs140/source_block-Class.md)