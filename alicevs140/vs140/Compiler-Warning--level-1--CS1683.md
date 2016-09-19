---
title: "Compiler Warning (level 1) CS1683"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: b3bd2729-a9e3-4b00-9937-d8d859fe87ef
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1683
Reference to type 'Type Name' claims it is defined in this assembly, but it is not defined in source or any added modules  
  
 This error can occur when you are importing an assembly that contains a reference back to the assembly you are currently compiling, but the assembly being compiled contains nothing matching the reference. One way to get to this situation is to compile your assembly, which initially does contain the member that the assembly being imported is referencing. Then you update your assembly, mistakenly removing the members that the imported assembly is referencing.