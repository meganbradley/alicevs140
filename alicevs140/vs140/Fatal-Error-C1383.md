---
title: "Fatal Error C1383"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ca224d14-d687-4fd6-80c2-8b82f28924ea
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1383
compiler option /GL is incompatible with the installed version of common language runtime  
  
 C1383 occurs when you are using a previous version of the common language runtime with a newer compiler, and when you compile with **/clr** and **/GL.**  
  
 To resolve, either do not use **/GL** with **/clr** or install the version of the common language runtime that shipped with your compiler.  
  
 For more information, see [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) and [/GL (Whole Program Optimization)](../Topic/-GL%20\(Whole%20Program%20Optimization\).md).