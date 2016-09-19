---
title: "Compiler Error CS1105"
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
ms.assetid: fcbd91ad-a76a-4b22-868d-16824fa96f85
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1105
Extension methods must be static.  
  
 Extension methods must be declared as static methods in a non-generic static class.  
  
## Example  
 The following example generates CS1105 because `Test` is not static:  
  
```  
// cs1105.cs  
// Compile with: /target:library  
public class Extensions  
{  
  
    // Single type parameter.  
        public void Test<T>(this System.String s) {} //CS1105  
  
}  
```  
  
## See Also  
 [Extension Methods (C# Programming Guide)](../Topic/Extension%20Methods%20\(C%23%20Programming%20Guide\).md)   
 [static (C# Reference)](../vs140/static--C#-Reference-.md)