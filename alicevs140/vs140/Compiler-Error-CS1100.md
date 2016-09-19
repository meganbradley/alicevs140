---
title: "Compiler Error CS1100"
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
ms.assetid: ea233371-36b6-49ae-a98c-a00ee3b79e53
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1100
Method 'name' has a parameter modifier 'this' which is not on the first parameter.  
  
 The `this` modifier is allowed only on the first parameter of a method, which indicates to the compiler that the method is an extension method.  
  
### To correct this error  
  
1.  Remove the `this` modifier from all except the first parameter of the method.  
  
## Example  
 The following code generates CS1100 because a `this` parameter is modifying the second parameter:  
  
```  
// cs1100.cs  
static class Test  
{  
    static void ExtMethod(int i, this Test c) // CS1100  
    {  
    }  
}  
```  
  
## See Also  
 [Extension Methods (C# Programming Guide)](../Topic/Extension%20Methods%20\(C%23%20Programming%20Guide\).md)