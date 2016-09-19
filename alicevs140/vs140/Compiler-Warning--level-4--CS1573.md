---
title: "Compiler Warning (level 4) CS1573"
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
ms.assetid: 1b68cb1a-9bfd-4343-b9b6-8ce195af5e23
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) CS1573
Parameter 'parameter' has no matching param tag in the XML comment for 'parameter' (but other parameters do)  
  
 When using the [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md) compiler option, a comment was specified for some but not all parameters in a method. You may have forgotten to enter a comment for these parameters.  
  
 The following sample generates CS1573:  
  
```  
// CS1573.cs  
// compile with: /W:4  
public class MyClass  
{  
   /// <param name='Int1'>Used to indicate status.</param>  
   // enter a comment for Char1?  
   public static void MyMethod(int Int1, char Char1)  
   {  
   }  
  
   public static void Main ()  
   {  
   }  
}  
```