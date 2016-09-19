---
title: "Compiler Error CS1946"
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
ms.topic: error-reference
ms.assetid: 4ccef263-1ae8-4065-ab46-25d14a38e24e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1946
An anonymous method expression cannot be converted to an expression tree.  
  
 An anonymous method represents a set of statements but an expression tree must not contain a statement. Therefore an anonymous method cannot be represented by an expression tree.  
  
### To correct this error  
  
1.  Change the anonymous method to a lambda expression.  
  
## Example  
 The following example generates CS1946:  
  
```  
// cs1946.cs  
using System;  
    using System.Linq.Expressions;  
  
    public delegate void D();  
  
    class Test  
    {  
        static void Main()  
        {  
            Expression<D> tree = delegate() { }; //CS1946  
            // Try using a lambda expression instead.  
            // Expression<D> tree = (x) => x + 1;  
        }  
    }  
```  
  
## See Also  
 [Anonymous Methods (C# Programming Guide)](../vs140/Anonymous-Methods--C#-Programming-Guide-.md)   
 [Expression Trees](../vs140/Expression-Trees--C#-and-Visual-Basic-.md)