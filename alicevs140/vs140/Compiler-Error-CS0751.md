---
title: "Compiler Error CS0751"
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
ms.assetid: 2ebaed5f-d3ca-452f-8fce-f3299b84360a
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0751
A partial method must be declared in a partial class or partial struct  
  
 It is not possible to declare a [partial](../vs140/partial--Method---C#-Reference-.md) method unless it is encapsulated inside a partial class or partial struct.  
  
### To correct this error  
  
1.  Either remove the `partial` modifier from the method and provide an implementation, or else add the `partial` modifier to the enclosing class or struct.  
  
## Example  
 The following example generates CS0751:  
  
```  
// cs0751.cs  
using System;  
  
public class C  
{  
    partial void Part(); // CS0751  
    public static int Main()  
    {  
        return 1;  
    }  
}  
```  
  
## See Also  
 [Partial Classes and Methods (C# Programming Guide)](../vs140/Partial-Classes-and-Methods--C#-Programming-Guide-.md)