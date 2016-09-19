---
title: "Compiler Warning (level 4) C4611"
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
ms.assetid: bd90d0a6-75f9-4e97-968d-dda6773e9fd8
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4611
interaction between 'function' and C++ object destruction is non-portable  
  
 On some platforms, functions that include **catch** may not support C++ object semantics of destruction when out of scope.  
  
 To avoid unexpected behavior, avoid using **catch** in functions that have constructors and destructors.  
  
 This warning is only issued once; see [pragma warning](../vs140/warning.md).