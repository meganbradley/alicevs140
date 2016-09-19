---
title: "task_from_result Function (Concurrency Runtime)"
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
ms.assetid: a989545d-9190-4396-a338-d632083a3ffc
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# task_from_result Function (Concurrency Runtime)
## Syntax  
  
```  
template<  
   typename _Ty  
>  
task<_Ty> task_from_result(  
   _Ty_Param,  
   const task_options& _TaskOptions = task_options()  
);  
  
inline task<bool> task_from_result(  
   bool _Param  
);  
  
inline task<void> task_from_result(  
   const task_options& _TaskOptions = task_options()  
);  
```  
  
#### Parameters  
 `_Ty`  
 `_Param`  
 `_TaskOptions`  
  
## Return Value  
  
## Requirements  
 **Header:** ppltasks.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)