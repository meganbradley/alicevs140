---
title: "choice::unlink_targets Method"
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
ms.assetid: a06d4a0e-f932-43d2-b595-e694a17b1b43
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# choice::unlink_targets Method
Unlinks all targets from this `choice` messaging block.  
  
## Syntax  
  
```  
virtual void unlink_targets();  
```  
  
## Remarks  
 This method does not need to be called from the destructor because destructor for the internal `single_assignment` block will unlink properly.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [choice Class](../vs140/choice-Class.md)