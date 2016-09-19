---
title: "Compiler Error CS0832"
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
ms.assetid: b5527209-a9bd-4f8c-a432-2e89bb1905d1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0832
An expression tree may not contain an assignment operator.  
  
 An expression tree does not preserve variable state or have any concept of a storage location.  
  
### To correct this error  
  
1.  Remove the assignment operator from the lambda or query expression.  
  
## Example  
 In the example code, as in all lambda expressions, `x` is just an input parameter being passed by value. Its value cannot be changed in an expression tree. It can be changed in a delegate lambda.  
  
```  
// cs0843.cs  
using System;  
using System.Linq;  
using System.Linq.Expressions;  
  
public class C  
{  
    public static int Main()  
    {  
        Expression<Func<int, int>> e = x => x += 5; // CS0843  
        return 1;  
    }  
}  
```