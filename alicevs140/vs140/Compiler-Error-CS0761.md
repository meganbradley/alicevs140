---
title: "Compiler Error CS0761"
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
ms.assetid: b16ac1df-0ddc-44d2-89f1-8d9c32af87ad
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0761
Partial method declarations of 'method<T\>' have inconsistent type parameter constraints.  
  
 If a partial method has an implementation, the generic type constraint must be identical to the constraint defined on the method signature.  
  
### To correct this error  
  
1.  Make the generic type constraints identical on each part of the partial method.  
  
## Example  
 The following code generates CS0761:  
  
```  
// cs0761.cs  
using System;  
  
public partial class C  
{  
    partial void Part<T>() where T : class;  
    partial void Part<T>() where T : struct // CS0761  
    {  
    }  
  
    public static int Main()  
    {  
        return 1;  
    }  
}  
  
```  
  
## See Also  
 [Partial Classes and Methods (C# Programming Guide)](../vs140/Partial-Classes-and-Methods--C#-Programming-Guide-.md)   
 [Constraints on Type Parameters (C# Programming Guide)](../Topic/Constraints%20on%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md)