---
title: "Compiler Error C2177"
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
ms.assetid: 2a39a880-cddb-4d3e-a572-645a14c4c478
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2177
constant too big  
  
 A constant value is too large for the variable type it is assigned.  
  
 The following sample generates C2177:  
  
```  
// C2177.cpp  
int main() {  
   int a=18446744073709551616;   // C2177  
   int b=18446744073709551615;   // OK  
}  
```