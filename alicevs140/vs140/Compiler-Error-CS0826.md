---
title: "Compiler Error CS0826"
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
ms.assetid: baa68741-2813-4bdd-9312-dd45fdf10701
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0826
No best type found for implicitly typed array.  
  
 Array elements must all be the same type or implicitly convertible to the same type according to the type inference rules used by the compiler. The best type must be one of the types present in the array expression. Elements will not be converted to a new type such as `object`. For an implicitly typed array, the compiler must infer the array type based on the type of elements assigned to it.  
  
### To correct this error  
  
-   Give the array an explicit type.  
  
-   Give all array elements the same type.  
  
-   Provide explicit casts on those elements that might be causing the problem.  
  
## Example  
 The following code generates CS0826 because the array elements are not all the same type, and the compiler's type inference logic does not find a single best type:  
  
```  
// cs0826.cs  
public class C  
{  
    public static int Main()  
    {  
        var x = new[] { 1, "str" }; // CS0826  
  
        char c = 'c';  
        short s1 = 0;  
        short s2 = -0;  
        short s3 = 1;  
        short s4 = -1;  
  
        var array1 = new[] { s1, s2, s3, s4, c, '1' }; // CS0826  
        return 1;  
    }  
}  
  
```  
  
## See Also  
 [Implicitly Typed Local Variables (C# Programming Guide)](../vs140/Implicitly-Typed-Local-Variables--C#-Programming-Guide-.md)