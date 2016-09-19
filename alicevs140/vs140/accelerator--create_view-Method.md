---
title: "accelerator::create_view Method"
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
ms.assetid: 8f405e0f-74c0-4868-8a22-ab6cbde72598
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# accelerator::create_view Method
Creates and returns an `accelerator_view` object on this accelerator, using the specified queuing mode. When the queuing mode is not specified, the new `accelerator_view` uses the [queuing_mode::immediate](../vs140/queuing_mode-Enumeration.md) queuing mode.  
  
## Syntax  
  
```  
accelerator_view create_view(  
   queuing_mode qmode = queuing_mode_automatic  
);  
```  
  
#### Parameters  
 `qmode`  
 The queuing mode.  
  
## Return Value  
 A new `accelerator_view` object on this accelerator, using the specified queuing mode.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [accelerator Class](../vs140/accelerator-Class.md)   
 [accelerator_view](../vs140/accelerator_view-Class.md)