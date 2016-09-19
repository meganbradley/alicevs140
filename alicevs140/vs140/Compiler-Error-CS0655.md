---
title: "Compiler Error CS0655"
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
ms.assetid: 8ce340e2-eeeb-476a-8609-ab4bbaf10c44
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0655
'parameter' is not a valid named attribute argument because it is not a valid attribute parameter type  
  
 See [Attributes (C# Programmers Reference)](../vs140/Attributes--C#-and-Visual-Basic-.md) for a discussion of valid parameter types for an attribute.  
  
## Example  
 The following sample generates CS0655:  
  
```  
// CS0655.cs  
using System;  
  
class MyAttribute : Attribute  
{  
    // decimal is not valid attribute parameter type  
    public decimal d = 0;  
    public int e = 0;  
}  
  
[My(d = 0)]   // CS0655  
// Try the following line instead:  
// [My(e = 0)]  
class C  
{  
    public static void Main()  
    {  
    }  
}  
```