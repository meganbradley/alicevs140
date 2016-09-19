---
title: "loop"
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
ms.assetid: 6d5bb428-cead-47e7-941d-7513bbb162c7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# loop
Controls how loop code is to be considered by the auto-parallelizer, and/or excludes a loop from consideration by the auto-vectorizer.  
  
## Syntax  
  
```  
  
#pragma loop( hint_parallel(n) )  
```  
  
```  
  
#pragma loop( no_vector )  
```  
  
```  
  
#pragma loop( ivdep )  
```  
  
#### Parameters  
 `hint_parallel(` `n` `)`  
 Hints to the compiler that this loop should be parallelized across `n` threads, where `n` is a positive integer literal or zero. If `n` is zero, the maximum number of threads is used at run time. This is a hint to the compiler, not a command, and there is no guarantee that the loop will be parallelized. If the loop has data dependencies, or structural issues—for example, the loop stores to a scalar that's used beyond the loop body—then the loop will not be parallelized.  
  
 The compiler ignores this option unless the [/Qpar](../Topic/-Qpar%20\(Auto-Parallelizer\).md) compiler switch is specified.  
  
 `no_vector`  
 By default, the auto-vectorizer is on and will attempt to vectorize all loops that it evaluates as benefitting from it. Specify this pragma to disable the auto-vectorizer for the loop that follows it.  
  
 `ivdep`  
 Hints to the compiler to ignore vector dependencies for this loop. Use this in conjunction with `hint_parallel`.  
  
## Remarks  
 To use the `loop` pragma, place it immediately before—not in—a loop definition. The pragma takes effect for the scope of the loop that follows it. You can apply multiple pragmas to a loop, in any order, but you must state each one in a separate pragma statement.  
  
## See Also  
 [Auto-Parallelization and Auto-Vectorization](../vs140/Auto-Parallelization-and-Auto-Vectorization.md)   
 [Pragma Directives and the __Pragma Keyword](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md)