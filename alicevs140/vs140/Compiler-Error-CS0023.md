---
title: "Compiler Error CS0023"
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
ms.assetid: 7a30073c-99de-41fa-ac6d-4a0dfbb76de9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0023
Operator 'operator' cannot be applied to operand of type 'type'  
  
 An attempt was made to apply an operator to a variable whose type was not designed to work with the operator. For more information, see [Data Types (C# Programmers Reference)](../Topic/Types%20\(C%23%20Programming%20Guide\).md) and [C# Operators](../Topic/C%23%20Operators.md).  
  
 The following sample generates CS0023:  
  
```  
// CS0023.cs  
namespace x  
{  
   public class a  
   {  
      public static void Main()  
      {  
         string s = "hello";  
         s = -s;   // CS0023, minus operator not allowed on strings  
      }  
   }  
}  
```