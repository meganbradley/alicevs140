---
title: "Compiler Warning (level 1 and level 4) C4949"
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
ms.assetid: 34f45a05-c115-49cb-9f67-0bd4f0735d9b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1 and level 4) C4949
pragmas 'managed' and 'unmanaged' are meaningful only when compiled with '/clr[:option]'  
  
 The compiler ignores the [managed](../vs140/managed--unmanaged.md) and unmanaged pragmas if the source code is not compiled with [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md). This warning is informational.  
  
 The following sample generates C4949:  
  
```  
// C4949.cpp  
// compile with: /LD /W1  
#pragma managed   // C4949  
```  
  
 When **#pragma unmanaged** is used without **/clr**, C4949 is a level 4 warning.  
  
 The following sample generates C4949:  
  
```  
// C4949b.cpp  
// compile with: /LD /W4  
#pragma unmanaged   // C4949  
```