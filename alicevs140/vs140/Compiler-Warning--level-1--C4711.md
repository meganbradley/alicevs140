---
title: "Compiler Warning (level 1) C4711"
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
ms.topic: error-reference
ms.assetid: 270506ab-fead-4328-b714-2978113be238
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4711
function 'function' selected for inline expansion  
  
 The compiler performed inlining on the given function, although it was not marked for inlining.  
  
 C4711 is enabled if [/Ob2](../Topic/-Ob%20\(Inline%20Function%20Expansion\).md) is specified.  
  
 Inlining is performed at the compiler's discretion. This warning is informational.  
  
 This warning is off by default. To enable a warning, use [#pragma warning](../vs140/warning.md). See [Compiler Warnings That Are Off by Default](../vs140/Compiler-Warnings-That-Are-Off-by-Default.md) for more information.