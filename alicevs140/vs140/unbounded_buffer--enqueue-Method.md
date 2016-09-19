---
title: "unbounded_buffer::enqueue Method"
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
ms.assetid: 14f43212-ca8d-4b13-a9d1-f46134ae26fd
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unbounded_buffer::enqueue Method
Adds an item to the `unbounded_buffer` messaging block.  
  
## Syntax  
  
```  
bool enqueue(  
   _Type const& _Item  
);  
```  
  
#### Parameters  
 `_Item`  
 The item to add.  
  
## Return Value  
 `true` if the item was accepted, `false` otherwise.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [unbounded_buffer Class](../vs140/unbounded_buffer-Class.md)