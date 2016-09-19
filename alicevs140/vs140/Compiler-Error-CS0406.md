---
title: "Compiler Error CS0406"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9d69681c-e261-4e5e-9361-ea566de12f2e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0406
The class type constraint 'constraint' must come before any other constraints  
  
 When a generic type or method has a class type constraint, that constraint must be listed first. To avoid this error, move the class type constraint to the beginning of the constraint list.  
  
## Example  
 The following sample generates CS0406.  
  
```  
// CS0406.cs  
// compile with: /target:library  
interface I {}  
class C {}  
class D<T> where T : I, C {}   // CS0406  
class D2<T> where T : C, I {}   // OK  
```