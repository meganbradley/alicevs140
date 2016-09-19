---
title: "Compiler Warning (level 1) C4177"
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
ms.assetid: 2b05a5b3-696e-4f21-818e-227b9335e748
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4177
\#pragma pragma should be at global scope  
  
 The [pragma](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md) pragma should not be used within a local scope. The **pragma** will not be valid until global scope is encountered after the current scope.  
  
 The following sample generates C4177:  
  
```  
// C4177.cpp  
// compile with: /W1  
// #pragma bss_seg("global")   // OK  
  
int main() {  
   #pragma bss_seg("local")    // C4177  
}  
```