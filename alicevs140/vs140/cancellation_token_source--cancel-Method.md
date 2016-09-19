---
title: "cancellation_token_source::cancel Method"
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
ms.assetid: 9e438b95-d38e-49b4-b716-46034623515d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# cancellation_token_source::cancel Method
Cancels the token. Any `task_group`, `structured_task_group`, or `task` which utilizes the token will be canceled upon this call and throw an exception at the next interruption point.  
  
## Syntax  
  
```  
void cancel() const;  
```  
  
## Requirements  
 **Header:** pplcancellation_token.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [cancellation_token_source Class](../vs140/cancellation_token_source-Class.md)