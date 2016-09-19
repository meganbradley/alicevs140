---
title: "Compiler Error CS2020"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b2db7a05-5965-4a9b-86c3-0c4792b29a6c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS2020
Only the first set of input files can build a target other than 'module'  
  
 In a multi-output compilation, the first output file must be built with [/target:exe](../vs140/-target-exe--C#-Compiler-Options-.md), [/target:winexe](../Topic/-target:winexe%20\(C%23%20Compiler%20Options\).md), or [/target:library](../vs140/-target-library--C#-Compiler-Options-.md). Any subsequent output files must be built with [/target:module](../vs140/-target-module--C#-Compiler-Options-.md).