---
title: "d3d_access_try_lock Function"
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
ms.assetid: a3050c34-df4b-4412-878a-626b2b431447
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# d3d_access_try_lock Function
Attempt to acquire the D3D access lock on an accelerator_view without blocking.  
  
## Syntax  
  
```  
bool __cdecl d3d_access_try_lock(  
   accelerator_view &_Av  
);  
```  
  
#### Parameters  
 `_Av`  
 The accelerator_view to lock.  
  
## Return Value  
 true if the lock was acquired, or false if it is currently held by another thread.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** concurrency::direct3d  
  
## See Also  
 [concurrency::direct3d Namespace](../vs140/Concurrency--direct3d-Namespace.md)