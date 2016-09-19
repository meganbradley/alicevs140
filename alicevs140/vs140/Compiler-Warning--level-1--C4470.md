---
title: "Compiler Warning (level 1) C4470"
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
ms.assetid: f52a3eaa-a235-4747-a47d-9ec4ad4cb0ea
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4470
floating-point control pragmas ignored under /clr  
  
 The float-control pragmas:  
  
-   [fenv_access](../vs140/fenv_access.md)  
  
-   [float_control](../vs140/float_control.md)  
  
-   [fp_contract](../vs140/fp_contract.md)  
  
 have no effect under [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md).  
  
 The following sample generates C4470:  
  
```  
// C4470.cpp  
// compile with: /clr /W1 /LD  
#pragma float_control(except, on)   // C4470  
```