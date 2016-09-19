---
title: "Compiler Error C3874"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: fd55fc05-69a7-4237-b3b7-dca1d5400b4f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3874
return type of 'function' should be 'int' instead of 'type'  
  
 A function does not have the return type that was expected by the compiler.  
  
 The following sample generates C3874:  
  
```  
// C3874b.cpp  
double main()  
{   // C3874  
}  
```