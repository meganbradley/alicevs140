---
title: "Compiler Warning (level 1) C4052"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f9955421-16ab-46e5-8f9d-bf1639a519ef
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4052
function declarations different; one contains variable arguments  
  
 One declaration of the function does not contain variable arguments. It is ignored.  
  
 The following sample generates C4052:  
  
```  
// C4052.c  
// compile with: /W4 /c  
int f();  
int f(int i, ...);   // C4052  
```