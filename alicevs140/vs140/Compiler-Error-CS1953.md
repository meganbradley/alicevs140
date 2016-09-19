---
title: "Compiler Error CS1953"
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
ms.assetid: b8af5eed-0f3b-4258-b4e2-f5d184288239
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1953
An expression tree lambda may not contain a method group.  
  
 A method call requires the `()` operator. The method name without that operator refers to the method group, which is the set of all the overloaded methods with that name.  
  
### To correct this error  
  
1.  If you meant to call the method, add the `()` operator.  
  
## Example  
 The following example generates CS1953:  
  
```  
// cs1953.cs  
using System;  
using System.Linq.Expressions;  
class CS1953  
{  
    public static void Main()  
    {  
        double num = 10;  
        Expression<Func<bool>> testExpr =  
              () => num.GetType is int; // CS1953   
    }  
}  
```