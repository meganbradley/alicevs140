---
title: "Compiler Error CS1529"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 672a6fd1-3a1f-422c-a29f-46f196d15211
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1529
A using clause must precede all other elements defined in the namespace except extern alias declarations  
  
 A [using](../vs140/using--C#-Reference-.md) clause must appear first in a namespace.  
  
## Example  
 The following sample generates CS1529:  
  
```  
// CS1529.cs  
namespace X  
{  
    namespace Subspace  
    {  
        using Microsoft;  
  
        class SomeClass  
        {  
        };  
  
        using Microsoft;      // CS1529, place before class definition  
    }  
  
    using System.Reflection;  // CS1529, place before namespace 'Subspace'  
}  
  
using System;                 // CS1529, place at the beginning of the file  
```