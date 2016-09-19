---
title: "Compiler Error CS0729"
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
ms.assetid: e0421d06-e818-404f-af97-d101272f4d07
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0729
Type 'type' is defined in this assembly, but a type forwarder is specified for it  
  
 You cannot use a type forwarder for a type defined in the same assembly.  
  
## Example  
 The following sample generates CS0729.  
  
```  
// CS0729.cs  
// compile with: /target:library  
using System.Runtime.CompilerServices;  
[assembly:TypeForwardedTo(typeof(TestClass))]   // CS0729  
class TestClass {}  
```