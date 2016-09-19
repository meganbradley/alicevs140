---
title: "Optimizing Your Code"
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
ms.assetid: 4f33e6c7-9870-43b3-9c2f-d7e44f764971
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Optimizing Your Code
By optimizing an executable, you can achieve a balance between fast execution speed and small code size. This topic discusses some of the mechanisms that Visual C++ provides to help you optimize code.  
  
## Language Features  
 The following topics describe some of the optimization features in the C/C++ language.  
  
 [Optimization Pragmas and Keywords](../vs140/Optimization-Pragmas-and-Keywords.md)  
 A list of keywords and pragmas that you can use in your code to improve performance.  
  
 [Compiler Options Listed by Category](../vs140/Compiler-Options-Listed-by-Category.md)  
 A list of **/O** compiler options that specifically affect execution speed or code size.  
  
 [Rvalue Reference Declarator: &&](../vs140/Rvalue-Reference-Declarator----.md)  
 Rvalue references support the implementation of *move semantics*. If move semantics are used to implement template libraries, the performance of applications that use those templates can significantly improve.  
  
### The optimize Pragma  
 If an optimized section of code causes errors or a slowdown, you can use the [optimize](../vs140/optimize.md) pragma to turn off optimization for that section.  
  
 Enclose the code between two pragmas, as follows.  
  
```  
#pragma optimize("", off)  
// some code here   
#pragma optimize("", on)  
```  
  
## Programming Practices  
 You might notice additional warning messages when you compile your code with optimization. This behavior is expected because some warnings relate only to optimized code. You can avoid many optimization problems if you heed these warnings.  
  
 Paradoxically, optimizing a program for speed could cause code to run slower. This is because some optimizations for speed increase code size. For example, inlining functions eliminates the overhead of function calls. However, inlining too much code might make your program so large that the number of virtual-memory page faults increases. Therefore, the speed gained from eliminating function calls may be lost to memory swapping.  
  
 The following topics discuss good programming practices.  
  
 [Tips for Improving Time-Critical Code](../vs140/Tips-for-Improving-Time-Critical-Code.md)  
 Better coding techniques can yield better performance. This topic suggests coding techniques that can help you make sure that the time-critical parts of your code perform satisfactorily.  
  
 [Optimization Best Practices](../vs140/Optimization-Best-Practices.md)  
 Provides general guidelines about how best to optimize your application.  
  
## Debugging Optimized Code  
 Because optimization might change the code created by the compiler, we recommend that you debug your application and measure its performance, and then optimize your code.  
  
 The following topics provide basic information about how to debug.  
  
-   [Debugging in Visual Studio](../vs140/Debugging-in-Visual-Studio.md)  
  
-   [Common Problems When Creating a Release Build](../vs140/Common-Problems-When-Creating-a-Release-Build.md)  
  
 The following topics provide more advanced information about how to debug.  
  
-   [How to: Debug Optimized Code](../vs140/How-to--Debug-Optimized-Code.md)  
  
-   [Why Floating-Point Numbers May Lose Precision](../vs140/Why-Floating-Point-Numbers-May-Lose-Precision.md)  
  
 The following assortment of topics provide information about how to optimize building, loading, and executing your code.  
  
-   [Improving Compiler Throughput](../vs140/Improving-Compiler-Throughput.md)  
  
-   [Using Function Name Without () Produces No Code](../vs140/Using-Function-Name-Without----Produces-No-Code.md)  
  
-   [Optimizing Inline Assembly](../vs140/Optimizing-Inline-Assembly.md)  
  
-   [Specifying Compiler Optimization for an ATL Project](../vs140/Specifying-Compiler-Optimization-for-an-ATL-Project.md)  
  
-   [What optimization techniques should I use to improve the client application's performance when loading?](../vs140/What-optimization-techniques-should-I-use-to-improve-the-client-application-s-performance-when-loading-.md)  
  
-   [!INCLUDE[crabout](../vs140/includes/crabout_md.md)] how to reduce the time to load DLL methods, see "Optimizing DLL Load Time Performance" in the "Under the Hood" column in the "MSDN Magazine" on the [MSDN Library](http://go.microsoft.com/fwlink/?linkid=556) Web site.  
  
-   [!INCLUDE[crabout](../vs140/includes/crabout_md.md)] how to minimize paging in applications, see "Improving Runtime Performance with the Smooth Working Set Tool" and "Improving Runtime Performance with the Smooth Working Set Tool—Part 2" in the "Bugslayer" column in the "MSDN Magazine" on the [MSDN Library](http://go.microsoft.com/fwlink/?linkid=556) Web site.  
  
## See Also  
 [C/C++ Building Reference](../vs140/C-C---Building-Reference.md)