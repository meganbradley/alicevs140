---
title: "Compiler Error CS0221"
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
ms.assetid: 97170b49-54f1-4dac-a865-2f9cc6bf55b1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0221
Constant value 'value' cannot be converted to a 'type' (use 'unchecked' syntax to override)  
  
 An assignment operation that would result in a data loss was detected by [checked](../vs140/checked--C#-Reference-.md), which is on by default. Either correct the assignment or use [unchecked](../vs140/unchecked--C#-Reference-.md) to resolve this error. For more information, see [Checked and Unchecked (C# Programmers Reference)](../vs140/Checked-and-Unchecked--C#-Reference-.md).  
  
 The following sample generates CS0221:  
  
```  
// CS0221.cs  
public class MyClass  
{  
   public static void Main()  
   {  
      // unchecked  
      // {  
         int a = (int)0xFFFFFFFF;   // CS0221  
         a++;  
      // }  
   }  
}  
```