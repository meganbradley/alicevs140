---
title: "Compiler Warning (level 1) C4182"
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
ms.assetid: 8970f3c6-e2dd-407e-b2ec-964360eb8b43
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4182
\#include nesting level is 'number' deep; possible infinite recursion  
  
 The compiler ran out of space on the heap because of the number of nested include files. An include file is nested when it is included from another include file.  
  
 This message is informational and precedes error [C1076](../vs140/Fatal-Error-C1076.md).