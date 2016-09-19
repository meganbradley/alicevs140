---
title: "Compiler Error CS1938"
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
ms.assetid: fc8de996-f7a1-46e8-b07b-aea520b391b9
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1938
The name 'name' is not in scope on the right side of 'equals'. Consider swapping the expressions on either side of 'equals'.  
  
 The `equals` keyword is a special operator that is used in a `join` clause to determine equality between two expressions. The range variable for the left side source sequence is in scope on the left side of equals, and the range variable for the right side source is only in scope on the left side of equals. You can verify this by experimenting with IntelliSense in the following code example.  
  
### To correct this error  
  
1.  Swap the position of the two range variables as shown in the commented line in the following example:  
  
## Example  
 The following code generates CS1938:  
  
```  
// cs1938.cs  
using System.Linq;  
class Test  
{  
    static void Main()  
    {  
        int[] sourceA = { 1, 2, 3, 4, 5 };  
        int[] sourceB = { 3, 4, 5, 6, 7 };  
  
        var query = from a in sourceA  
                    join b in sourceB on b equals a // CS1938  
                    // Try the following line instead.  
                    // join b in sourceB on a equals b  
                    select new { a, b };  
    }  
}  
```  
  
## See Also  
 [join clause (C# Reference)](../Topic/join%20clause%20\(C%23%20Reference\).md)