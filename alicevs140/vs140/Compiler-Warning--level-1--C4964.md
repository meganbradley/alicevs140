---
title: "Compiler Warning (level 1) C4964"
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
ms.assetid: b89c9274-8a92-4b7c-aa30-3fbb1b68ac73
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4964
No optimization options were specified; profile info will not be collected  
  
 [/GL](../Topic/-GL%20\(Whole%20Program%20Optimization\).md) and [/LTCG](../vs140/-LTCG--Link-time-Code-Generation-.md) were specified, but no optimizations were requested, so no .pgc files will be generated and, therefore, no profile-guided optimizations will be possible.  
  
 If you want .pgc files to be generated when you run your application, specify one of the [/O](../vs140/-O-Options--Optimize-Code-.md) compiler options.  
  
 The following sample generates C4964:  
  
```  
// C4964.cpp  
// compile with: /W1 /GL /link /ltcg:pgi  
// C4964 expected  
// Add /O2, for example, to the command line to resolve this warning.  
int main() {  
   int i;  
}  
```