---
title: "accelerator_view::wait Method"
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
ms.assetid: c34ac1b3-e5bf-4a4e-86a3-420d23f0e2e9
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# accelerator_view::wait Method
Waits for all commands submitted to the  [accelerator_view](../vs140/accelerator_view-Class.md) object to finish.  
  
## Syntax  
  
```  
void wait();  
```  
  
## Return Value  
 Returns `void`.  
  
## Remarks  
 If the  [queuing_mode](../vs140/queuing_mode-Enumeration.md) is `immediate`, this method returns immediately without blocking.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [accelerator_view Class](../vs140/accelerator_view-Class.md)