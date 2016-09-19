---
title: "Compiler Error CS1106"
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
ms.assetid: 3585600a-6b2c-47aa-a418-ef049f07c107
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1106
Extension methods must be defined in a non generic static class.  
  
 Extension methods must be defined as static methods in a non-generic static class.  
  
## Example  
 The following example generates CS1106 because the class `Extensions` is not defined as `static`:  
  
```  
// cs1106.cs  
public class Extensions // CS1106  
{  
    public  static void Test<T>(this System.String s) {}  
}  
```  
  
## See Also  
 [Extension Methods (C# Programming Guide)](../Topic/Extension%20Methods%20\(C%23%20Programming%20Guide\).md)   
 [static (C# Reference)](../vs140/static--C#-Reference-.md)