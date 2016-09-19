---
title: "accelerator::get_is_emulated Method"
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
ms.assetid: db25b773-6342-4870-912a-454392cf3e5c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# accelerator::get_is_emulated Method
Determines whether the [accelerator](../vs140/accelerator-Class.md) is emulated.  
  
## Syntax  
  
```  
bool get_is_emulated() const;  
```  
  
## Return Value  
 `true` if the `accelerator` is emulated. Otherwise, `false`.  
  
## Remarks  
 The Direct3D reference and WARP accelerators, for example, are emulated.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [accelerator Class](../vs140/accelerator-Class.md)