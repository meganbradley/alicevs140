---
title: "Compiler Error CS1542"
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
ms.assetid: d7f60aa2-6645-472c-ac12-fa57a09fbd87
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1542
'dll' cannot be added to this assembly because it already is an assembly; use '/R' option instead  
  
 The file that was referenced with the [/addmodule](../Topic/-addmodule%20\(C%23%20Compiler%20Options\).md) compiler option was not built with [/target:module](../vs140/-target-module--C#-Compiler-Options-.md); use [/reference](../vs140/-reference--C#-Compiler-Options-.md) to reference the file in this compilation.