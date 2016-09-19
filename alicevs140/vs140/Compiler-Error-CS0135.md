---
title: "Compiler Error CS0135"
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
ms.assetid: 1bda402c-e8bd-4117-93d9-f4968d9e8303
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0135
'declaration1' conflicts with the declaration 'declaration2'  
  
 The compiler does not allow hiding names, which commonly leads to logic errors in your code.  
  
## Example  
 The following sample generates CS0135:  
  
```  
// CS0135.cs  
public class MyClass2  
{  
   public static int i = 0;  
  
   public static void Main()  
   {  
      {  
         int i = 4;  
         i++;  
      }  
      i = 0;   // CS0135  
   }  
}  
```  
  
 From the [C# Language Specification](../vs140/C#-Language-Specification.md), Section 7.5.2.1:  
  
 For each occurrence of a given identifier as a simple-name in an expression or declarator, within the local variable declaration space (§3.3) immediately enclosing that occurrence, every other occurrence of the same identifier as a simple-name in an expression or declarator must refer to the same entity. This rule ensures that the meaning of a name is always the same within a given block, switch block, for-, foreach- or using-statement, or anonymous function.