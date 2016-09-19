---
title: "Compiler Error CS0196"
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
ms.assetid: d361484e-73b8-439a-99c7-714e61d73755
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0196
A pointer must be indexed by only one value  
  
 A pointer cannot have multiple indices. For more information, see [Pointer types (C# Programmers Reference)](../vs140/Pointer-types--C#-Programming-Guide-.md)  
  
 The following sample generates CS0196:  
  
```  
// CS0196.cs  
public class MyClass  
{  
   public static void Main ()  
   {  
      int *i = null;  
      int j = 0;  
      j = i[1,2];   // CS0196  
      // try the following line instead  
      // j = i[1];  
   }  
}  
```