---
title: "C++ AMP (C++ Accelerated Massive Parallelism)"
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
ms.assetid: e27824cb-3167-409b-8c3f-a0e476d8f349
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C++ AMP (C++ Accelerated Massive Parallelism)
C++ AMP (C++ Accelerated Massive Parallelism) accelerates the execution of your C++ code by taking advantage of the data-parallel hardware that's commonly present as a graphics processing unit (GPU) on a discrete graphics card. The C++ AMP programming model includes support for multidimensional arrays, indexing, memory transfer, and tiling. It also includes a mathematical function library. You can use C++ AMP language extensions to control how data is moved from the CPU to the GPU and back.  
  
## Related Topics  
  
|Title|Description|  
|-----------|-----------------|  
|[Overview of C++ AMP](../vs140/C---AMP-Overview.md)|Describes the key features of C++ AMP and the mathematical library.|  
|[Using Lambdas, Function Objects, and Restricted Functions](../vs140/Using-Lambdas--Function-Objects--and-Restricted-Functions.md)|Describes how to use lambda expressions, function objects, and restricted functions in calls to the [parallel_for_each](../vs140/parallel_for_each-Function--C---AMP-.md) method.|  
|[Using Tiles](../vs140/Using-Tiles.md)|Describes how to use tiles to accelerate your C++ AMP code.|  
|[Using accelerator and accelerator_view objects](../vs140/Using-accelerator-and-accelerator_view-Objects.md)|Describes how to use accelerators to customize execution of your code on the GPU.|  
|[Using C++ AMP in Windows Store Apps](../vs140/Using-C---AMP-in-Windows-Store-Apps.md)|Describes how to use C++ AMP in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps that use Windows Runtime types.|  
|[Graphics (C++ AMP)](../vs140/Graphics--C---AMP-.md)|Describes how to use the C++ AMP graphics library.|  
|[Walkthrough: Matrix Multiplication](../vs140/Walkthrough--Matrix-Multiplication.md)|Demonstrates matrix multiplication using C++ AMP code and tiling.|  
|[Walkthrough: Debugging a C++ AMP Application](../vs140/Walkthrough--Debugging-a-C---AMP-Application.md)|Explains how to create and debug an application that uses parallel reduction to sum up a large array of integers.|  
  
## Reference  
 [Reference (C++ Accelerated Massive Parallelism)](../vs140/Reference--C---AMP-.md)  
  
 [tile_static Keyword](../vs140/tile_static-Keyword.md)  
  
 [Restriction Clause (C++ Accelerated Massive Parallelism)](../vs140/restrict--C---AMP-.md)  
  
## Other Resources  
 [Parallel Programming in Native Code Blog](http://go.microsoft.com/fwlink/p/?LinkId=238472)  
  
 [C++ AMP sample projects for download](http://go.microsoft.com/fwlink/p/?LinkId=248508)  
  
 [Analyzing C++ AMP Code with the Concurrency Visualizer](http://go.microsoft.com/fwlink/?LinkID=253987&clcid=0x409)