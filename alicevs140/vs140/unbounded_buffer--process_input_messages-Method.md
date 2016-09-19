---
title: "unbounded_buffer::process_input_messages Method"
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
ms.assetid: 79725aaa-674c-4d78-8a00-759749b9c6a0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unbounded_buffer::process_input_messages Method
Places the `message``_PMessage` in this `unbounded_buffer` messaging block and tries to offer it to all of the linked targets.  
  
## Syntax  
  
```  
virtual void process_input_messages(  
   _Inout_ message<_Type> * _PMessage  
);  
```  
  
#### Parameters  
 `_PMessage`  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [unbounded_buffer Class](../vs140/unbounded_buffer-Class.md)