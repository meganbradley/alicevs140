---
title: "Compiler Warning (level 1) CS3000"
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
ms.assetid: 37cdd3dc-8481-4e29-b78c-281baeca2d64
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS3000
Methods with variable arguments are not CLS-compliant  
  
 The arguments used in the method expose features that are not in the Common Language Specifications (CLS). For more information on CLS Compliance, see [Writing CLS-Compliant Code](assetId:///4c705105-69a2-4e5e-b24e-0633bc32c7f3).  
  
 The following example generates the warning CS3000.  
  
```  
// CS3000.cs  
// compile with: /target:library  
// CS3000 expected  
[assembly:System.CLSCompliant(true)]  
  
public class Test  
{  
   public void AddABunchOfInts( __arglist ) {}   // CS3000  
}  
```