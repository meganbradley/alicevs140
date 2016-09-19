---
title: "Compiler Error CS1032"
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
ms.assetid: fe318a6c-4403-4b9b-b3d8-753ec31c00ff
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1032
Cannot define/undefine preprocessor symbols after first token in file  
  
 The `#define` and `#undef` [preprocessor directives](../vs140/C#-Preprocessor-Directives.md) must be used at the beginning of a program, before any other keywords, such as those used in the namespace declaration.  
  
 The following sample generates CS1032:  
  
```  
// CS1032.cs  
namespace x  
{  
   public class clx  
   {  
      #define a   // CS1032, put before namespace  
      public static void Main()  
      {  
      }  
   }  
}  
```