---
title: "Compiler Warning (level 3) C4557"
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
ms.assetid: 7d9db716-03b2-4ee5-9b09-ba8aa5aa7e4c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4557
'__assume' contains effect 'effect'  
  
 The value passed to an [__assume](../vs140/__assume.md) statement2 was modified.  
  
 This warning is off by default. See [Compiler Warnings That Are Off by Default](../vs140/Compiler-Warnings-That-Are-Off-by-Default.md) for more information.  
  
 The following sample generates C4557:  
  
```  
// C4557.cpp  
// compile with: /W3  
#pragma warning(default : 4557)  
int main()  
{  
   int i;  
   __assume(i++);   // C4557  
}  
```