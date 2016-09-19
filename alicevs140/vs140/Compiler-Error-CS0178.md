---
title: "Compiler Error CS0178"
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
ms.assetid: 73e48648-6c0c-4987-92ca-fb2015a38910
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0178
Invalid rank specifier: expected ',' or ']'  
  
 An array initialization was ill-formed. For example, when specifying the array dimensions, you can specify the following:  
  
-   A number in brackets  
  
-   Empty brackets  
  
-   A comma enclosed in brackets  
  
 For more information, see [Arrays (C# Programmer's Reference)](../Topic/Arrays%20\(C%23%20Programming%20Guide\).md) and the C# specification ([C# Language Specification](../vs140/C#-Language-Specification.md)) section on array initializers.  
  
## Example  
 The following sample generates CS0178.  
  
```  
// CS0178.cs  
class MyClass  
{  
   public static void Main()  
   {  
      int a = new int[5][,][][5;   // CS0178  
      int[,] b = new int[3,2];   // OK  
  
      int[][] c = new int[10][];  
      c[0] = new int[5][5];   // CS0178  
      c[0] = new int[2];   // OK  
      c[1] = new int[2]{1,2};   // OK  
   }  
}  
```