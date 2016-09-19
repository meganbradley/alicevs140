---
title: "Compiler Error CS1933"
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
ms.assetid: 80d719d3-1b39-44ec-90fd-039ae5570f01
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1933
Expression cannot contain query expressions  
  
 Some variables cannot be initialized with a query expression. Constants cannot be initialized with query expressions because constants may only be initialized with some combination of literals, named constants, and mathematical operators.  
  
### To correct this error  
  
1.  Remove the modifier from the query variable.  
  
## Example  
 The following example generates CS1933:  
  
```  
// cs1933.cs  
using System.Linq;  
using System.Collections;  
  
class P  
{  
    const IEnumerable e = from x in new[] { 1, 2, 3 } select x; // CS1933  
    static int Main()  
    {  
        return 1;  
    }  
}  
```  
  
## See Also  
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)