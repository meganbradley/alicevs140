---
title: "Compiler Error CS1104"
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
ms.assetid: 65bfe85f-8dd1-4aed-bcd1-1f7e0635868c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1104
A parameter array cannot be used with 'this' modifier on an extension method.  
  
 The first parameter of an extension method cannot be a params array.  
  
### To correct this error  
  
1.  Remember that the first parameter of an extension method definition specifies which type the method will "extend". It is not an input parameter. Therefore, it makes no sense to have a params array in this location. If you do have to pass in a params array, make it the second parameter.  
  
## Example  
 The following example generates CS1104:  
  
```  
// cs1104.cs  
// Compile with: /target:library  
public static class Extensions  
{  
    public static void Test<T>(this params T[] tArr) {} // CS1104  
}   
```  
  
## See Also  
 [Extension Methods (C# Programming Guide)](../Topic/Extension%20Methods%20\(C%23%20Programming%20Guide\).md)   
 [params (C# Reference)](../vs140/params--C#-Reference-.md)