---
title: "Compiler Error CS0582"
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
ms.assetid: cc0f4c75-c41d-423e-a4dc-e55a124f5cae
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0582
The Conditional not valid on interface members  
  
 **ConditionalAttribute** is not valid on an interface member.  
  
 The following sample generates CS0582:  
  
```  
// CS0582.cs  
// compile with: /target:library  
using System.Diagnostics;  
interface MyIFace  
{  
   [ConditionalAttribute("DEBUG")]   // CS0582  
   void zz();  
}  
```