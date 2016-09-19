---
title: "Compiler Error CS0828"
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
ms.assetid: e18ffe72-2fcc-436d-be7f-8c8365b86129
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0828
Cannot assign 'expression' to anonymous type property.  
  
 An anonymous type cannot be initialized with a null value or an unsafe type, or a method group or anonymous function.  
  
### To correct this error  
  
1.  Either add a type declaration to the left side of the assignment, or change the expression on the right side so that it has an acceptable type.  
  
## Example  
 The following code generates CS0828 because a member of an anonymous type cannot be initialized with a null value.  
  
```  
// cs0828.cs  
using System;  
  
public class C  
{  
    public static int Main()  
    {  
        var a = 1;  
        var c = new { p1 = null }; // CS0828  
        return 1;  
    }  
}  
```  
  
## See Also  
 [Implicitly Typed Local Variables (C# Programming Guide)](../vs140/Implicitly-Typed-Local-Variables--C#-Programming-Guide-.md)