---
title: "cancellation_token_source::get_token Method"
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
ms.assetid: b532dbe1-50a9-4431-bf59-ce97fdcc7b6f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# cancellation_token_source::get_token Method
Returns a cancellation token associated with this source. The returned token can be polled for cancellation or provide a callback if and when cancellation occurs.  
  
## Syntax  
  
```  
cancellation_token get_token() const;  
```  
  
## Return Value  
 A cancellation token associated with this source.  
  
## Requirements  
 **Header:** pplcancellation_token.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [cancellation_token_source Class](../vs140/cancellation_token_source-Class.md)