---
title: "Compiler Error CS0692"
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
ms.assetid: d2fd650b-1f84-44b1-8c7e-471cad92a85e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0692
Duplicate type parameter 'identifier'  
  
 The same name may not be used more than once in a type parameter list. Rename or remove the duplicate type parameter(s).  
  
## Example  
 The following sample generates CS0692:  
  
```  
// CS0692.cs  
// compile with: /target:library  
class C <T, A, T>   // CS0692  
{  
}  
  
class D <T, T>   // CS0692  
{  
}  
```