---
title: "Compiler Error CS1931"
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
ms.assetid: c0071c3d-ae11-4073-87df-508150daef68
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1931
The range variable 'variable' conflicts with a previous declaration of 'variable'.  
  
 The declaration of a range variable, just like every other declaration, must have an identifier which is unique within the variable's declaration space.  
  
### To correct this error  
  
1.  Give the range variable a unique name.  
  
## Example  
 The following code generates CS1931 because the identifier `x` is used both as a local variable in `Main` and as the range variable in the query expression:  
  
```  
// cs1931.cs  
class Test  
    {  
        static void Main()  
        {  
            int x = 1;  
            var y = from x in Enumerable.Range(1, 100) // CS1931  
                    select x;  
        }  
    }  
```  
  
## See Also  
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)