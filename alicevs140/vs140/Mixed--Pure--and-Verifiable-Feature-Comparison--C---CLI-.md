---
title: "Mixed, Pure, and Verifiable Feature Comparison (C++-CLI)"
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
H1: Mixed, Pure, and Verifiable Feature Comparison (C++/CLI)
ms.assetid: 3f7a82ba-0e69-4927-ba0c-fbc3160e4394
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Mixed, Pure, and Verifiable Feature Comparison (C++-CLI)
This topic compares features among the different **/clr** compilation modes. For more information, see [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md).  
  
## Feature Comparison  
  
|Feature|Mixed (/clr)|Pure (/clr:pure)|Safe (/clr:safe)|Related Information|  
|-------------|---------------------|-------------------------|-------------------------|-------------------------|  
|CRT library|supported|supported||[Run-Time Routines by Category](../vs140/Run-Time-Routines-by-Category.md)|  
|MFC/ATL|supported|||[MFC Reference](../vs140/MFC-Desktop-Applications.md) &#124; [ATL Class Overview](../vs140/ATL-Class-Overview.md)|  
|Unmanaged Functions|supported|||[Mixed Assemblies](../vs140/Mixed--Native-and-Managed--Assemblies.md)|  
|Unmanaged Data|supported|supported||[Pure and Verifiable Code](../vs140/Pure-and-Verifiable-Code--C---CLI-.md)|  
|Callable from Unmanaged Functions|supported|||[Migrating to /clr:pure](../vs140/How-to--Migrate-to--clr-pure--C---CLI-.md)|  
|Supports calling unmanaged Functions|supported|C-style functions only|P/Invoke only|[Using C++ Interop Features](../vs140/Using-C---Interop--Implicit-PInvoke-.md)|  
|Supports Reflection|DLLs only|supported|supported|[Reflection in C++](../Topic/Reflection%20\(C++-CLI\).md)|  
  
## See Also  
 [Pure and Verifiable Code](../vs140/Pure-and-Verifiable-Code--C---CLI-.md)