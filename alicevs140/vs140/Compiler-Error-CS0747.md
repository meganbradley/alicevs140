---
title: "Compiler Error CS0747"
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
ms.assetid: dc1b7e38-cee5-406c-b193-a60ec4faebe1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0747
Invalid initializer member declarator.  
  
 An object initializer is used to assign values to properties or fields. Any expression which is not an assignment to a property or field is a compile-time error.  
  
### To correct this error  
  
1.  Ensure that all expressions in the initializer are assignments to properties or fields of the type. In the following example, the second expression is an error because the value `1` is not assigned to any property or field of `List<int>`.  
  
## Example  
 The following code generates CS0747:  
  
```  
// cs0747.cs  
using System.Collections.Generic;  
  
public class C  
{  
    public static int Main()  
    {  
        var t = new List<int> { Capacity = 2, 1 }; // CS0747  
        return 1;  
    }  
}  
```  
  
## See Also  
 [Object and Collection Initializers (C# Programming Guide)](../Topic/Object%20and%20Collection%20Initializers%20\(C%23%20Programming%20Guide\).md)