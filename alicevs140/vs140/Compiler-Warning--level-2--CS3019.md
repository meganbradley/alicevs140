---
title: "Compiler Warning (level 2) CS3019"
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
ms.assetid: b41117cf-8956-4989-93fd-9903812e2d2f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS3019
CLS compliance checking will not be performed on 'type' because it is not visible from outside this assembly.  
  
 This warning occurs when a type or a member that has the <xref:System.CLSCompliantAttribute?qualifyHint=False> attribute is not visible from another assembly. To resolve this error, remove the attribute on any classes or members that are not visible from the other assembly, or make the type or members visible. For more information on CLS Compliance, see [<PAVE OVER\> Writing CLS-Compliant Code](assetId:///4c705105-69a2-4e5e-b24e-0633bc32c7f3).  
  
## Example  
 The following sample generates CS3019:  
  
```  
// CS3019.cs  
// compile with: /W:2  
  
using System;  
  
[assembly: CLSCompliant(true)]  
  
// To fix the error, remove the next line  
[CLSCompliant(true)]  // CS3019  
class C  
{  
    [CLSCompliant(false)]  // CS3019  
    void Foo()  
    {  
    }  
  
    static void Main()  
    {  
    }  
}  
```  
  
## See Also  
 [What Is the Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6)