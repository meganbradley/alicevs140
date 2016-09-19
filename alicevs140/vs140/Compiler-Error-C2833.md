---
title: "Compiler Error C2833"
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
ms.assetid: b9418ce1-e2ee-4599-8959-6fde89c27569
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2833
'operator operator' is not a recognized operator or type  
  
 The word `operator` must be followed by an operator that you want to override or a type you want to convert.  
  
 For a list of the operators that you can define in a managed type, see [User-defined Operators](../vs140/User-Defined-Operators--C---CLI-.md).  
  
 The following sample generates C2833:  
  
```  
// C2833.cpp  
// compile with: /c  
class A {};  
  
void operator ::* ();   // C2833  
void operator :: ();   // OK  
```