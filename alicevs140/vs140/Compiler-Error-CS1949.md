---
title: "Compiler Error CS1949"
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
ms.assetid: 959f553e-ac3d-43a1-b0a0-11e270f2ad64
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1949
The contextual keyword 'var' cannot be used in a range variable declaration.  
  
 A range variable is implicitly typed by the compiler. There is no need to use [var](../vs140/var--C#-Reference-.md) with a range variable.  
  
### To correct this error  
  
1.  Remove the `var` keyword from in front of the range variable.  
  
## Example  
 The following example generates CS1949:  
  
```  
// cs1949.cs  
using System;  
using System.Linq;  
class Test  
{  
    static void Main()  
    {  
        var x = from var i in Enumerable.Range(1, 100) // CS1949  
        select i;  
    }  
}  
```  
  
## See Also  
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [The Three Parts of a LINQ Query](../Topic/Introduction%20to%20LINQ%20Queries%20\(C%23\).md)