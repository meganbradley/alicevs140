---
title: "Compiler Error CS1027"
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
ms.assetid: a6657f0f-5664-47a5-95cf-803f5a0e0c90
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1027
\#endif directive expected  
  
 A matching `#endif` [preprocessor directive](../vs140/C#-Preprocessor-Directives.md) was not found for a specified `#if` directive. Or, the compiler may have found a `#endregion` directive when there was no matching `#region` directive inside a `#if` block.  
  
 The following sample generates CS1027:  
  
```  
// CS1027.cs  
#if true   // CS1027, uncomment next line to resolve  
// #endif  
  
namespace x  
{  
   public class clx  
   {  
      public static void Main()  
      {  
      }  
   }  
}  
```