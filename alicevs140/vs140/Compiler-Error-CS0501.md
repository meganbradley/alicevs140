---
title: "Compiler Error CS0501"
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
ms.assetid: 3ff45208-5b9b-42f6-8a12-1eb38a665f33
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0501
'member function' must declare a body because it is not marked abstract, extern, or partial  
  
 Nonabstract methods must have implementations.  
  
 The following sample generates CS0501:  
  
```  
// CS0501.cs  
// compile with: /target:library  
public class clx  
{  
   public void f();   // CS0501 declared but not defined  
   public void g() {}   // OK  
}  
```