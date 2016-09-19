---
title: "Compiler Error CS1947"
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
ms.assetid: e2822fba-a176-4466-9cdc-63c44e22ebcb
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1947
Range variable 'variable name' cannot be assigned to -- it is read only.  
  
 A range variable is like an iteration variable in a `foreach` statement. It cannot be assigned to in a query expression.  
  
### To correct this error  
  
1.  Remove the assignment to the range variable.  
  
2.  If necessary, introduce a new range variable by using the `let` clause and use it to store the value.  
  
## Example  
 The following code generates CS1947:  
  
```  
// cs1947.cs  
using System.Linq;  
class Test  
{  
    static void Main()  
    {  
        int[] array = new int[] { 1, 2, 3, 4, 5 };  
        var x = from i in array  
                let k = i  
                select i = 5; // CS1947  
        x.ToList();  
    }  
}  
```  
  
## See Also  
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)