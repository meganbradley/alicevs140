---
title: "Compiler Error CS0825"
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
ms.assetid: 49393d23-ec5f-4b44-a3fd-7e0a95ac0edd
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0825
The contextual keyword 'var' may only appear within a local variable declaration.  
  
 Implicit typing with the `var` keyword can only be applied to variables at local method scope.  
  
### To correct this error  
  
1.  If the variable belongs at class scope, give it an explicit type.  Otherwise move it inside the method where it will be used.  
  
## Example  
 The following code generates CS0825 because `var` is used on a class field:  
  
```  
// cs0825.cs  
class Test  
{  
    private var myField; //CS0825  
  
    static int Main()  
    {  
        var a = 1; // var is OK here  
        return -1;  
    }  
}  
```  
  
## See Also  
 [Implicitly Typed Local Variables (C# Programming Guide)](../vs140/Implicitly-Typed-Local-Variables--C#-Programming-Guide-.md)