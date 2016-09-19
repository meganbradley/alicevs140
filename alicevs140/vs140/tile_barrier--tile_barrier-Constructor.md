---
title: "tile_barrier::tile_barrier Constructor"
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
ms.assetid: 75891361-0a6a-4870-8b74-2ddeb9d50d5d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# tile_barrier::tile_barrier Constructor
Initializes a new instance of the [tile_barrier](../vs140/tile_barrier-Class.md) class by copying an existing one.  
  
## Syntax  
  
```  
tile_barrier(  
   const tile_barrier& _Other  
) restrict(amp,cpu);  
```  
  
#### Parameters  
 `_Other`  
 The `tile_barrier` object to copy.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [tile_barrier Class](../vs140/tile_barrier-Class.md)