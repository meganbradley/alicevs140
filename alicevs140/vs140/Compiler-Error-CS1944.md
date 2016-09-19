---
title: "Compiler Error CS1944"
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
ms.assetid: e5e2c018-9a7e-48ee-8dd3-98e3553777c1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1944
An expression tree may not contain an unsafe pointer operation  
  
 Expression trees do not support pointer types because the <xref:System.Linq.Expressions.Expression`1.Compile?qualifyHint=True> method is only allowed to produce verifiable code. See comments.  
  
### To correct this error  
  
1.  Do not use pointer types when you are trying to create an expression tree.  
  
## Example  
 The following example generates CS1944:  
  
```  
// cs1944.cs  
// Compile with: /unsafe  
using System.Linq.Expressions;  
unsafe class Test  
{  
    public delegate int* D(int i);  
    static void Main()  
    {  
        Expression<D> tree = x => &x; // CS1944  
    }  
}  
  
using System.Linq.Expressions;  
unsafe class Test  
{  
    public delegate int* D(int i);  
    static void Main()  
    {  
        Expression<D> tree = x => &x; // CS1944  
    }  
}  
```  
  
 In some situations it is okay to have pointers in expression trees. For example, consider the following code:  
  
 `Expression<Func<int*[], int*[]>) e = (int*[] i)=>i;`  
  
 This code is a valid expression tree because no type arguments are pointer types. They are arrays of pointers, and arrays are not pointer types. Also, the body of the expression tree does not do anything dangerous with any pointer.  
  
## See Also  
 [unsafe (C# Reference)](../vs140/unsafe--C#-Reference-.md)