---
title: "Compiler Error CS1952"
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
ms.assetid: 8c560bf9-df93-40f5-a3d8-c66b31cde08f
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1952
An expression tree lambda may not contain a method with variable arguments  
  
 The unsupported `__arglist` keyword is not allowed in lambda expressions that compile to expression trees.  
  
### To correct this error  
  
1.  Forget that you ever heard of `__arglist`.  
  
## Example  
 The following code produces CS1952:  
  
```  
// cs1952.cs  
using System;  
using System.Linq.Expressions;  
  
class Test  
{  
    public static int M(__arglist)  
    {  
        return 1;  
    }  
  
    static int Main()  
    {  
        Expression<Func<int, int>> f = x => Test.M(__arglist(x)); // CS1952  
        return 1;  
    }  
}  
  
```