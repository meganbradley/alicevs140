---
title: "Compiler Error CS1942"
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
ms.assetid: afbe5e8e-1944-416e-916b-39e2c373814b
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1942
The type of the expression in the 'clause' clause is incorrect. Type inference failed in the call to 'method'.  
  
 This error is typically generated when the range variable has been given an incorrect explicit type.  
  
### To correct this error  
  
1.  If the range variable is explicitly typed, make sure that the type is either the same as, or implicitly convertible from, the type of the elements in the collection it iterates. If the range variable is preceded with the `var` keyword, remove `var`.  
  
## Example  
 The following code generates CS1942:  
  
```  
// cs1942.cs  
class Program  
    {  
        static void Main(string[] args)  
        {  
            var x = from var i in Enumerable.Range(1, 100) // CS1949  
                    select i; //CS1942  
        }  
    }  
```  
  
 CS1942 is related to CS1949 because the use of `var` with a range variable causes the underlying `Cast<T>` operation to fail because `var` is not a type.  
  
## See Also  
 [var (C# Reference)](../vs140/var--C#-Reference-.md)   
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)