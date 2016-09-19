---
title: "completion_future::get Method"
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
ms.assetid: edfee0c5-cfdc-45fc-b115-e15057b1bb74
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# completion_future::get Method
Waits until the associated asynchronous operation completes. Throws the stored exception if one was encountered during the asynchronous operation.  
  
## Syntax  
  
```  
void get() const;  
```  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [completion_future Class](../vs140/completion_future-Class.md)