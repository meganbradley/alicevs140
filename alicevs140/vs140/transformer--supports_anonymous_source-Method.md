---
title: "transformer::supports_anonymous_source Method"
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
ms.assetid: 0b024c84-9927-472f-92e2-87035de58b4a
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# transformer::supports_anonymous_source Method
Overrides the `supports_anonymous_source` method to indicate that this block can accept messages offered to it by a source that is not linked.  
  
## Syntax  
  
```  
virtual bool supports_anonymous_source();  
```  
  
## Return Value  
 `true` because the block does not postpone offered messages.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [transformer Class](../vs140/transformer-Class.md)