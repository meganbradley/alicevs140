---
title: "Compiler Warning (level 4) CS1591"
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
ms.assetid: 53c8599e-3e83-4d17-998b-05c934704283
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) CS1591
Missing XML comment for publicly visible type or member 'Type_or_Member'  
  
 The [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md) compiler option was specified, but one or more constructs did not have comments.  
  
 The following sample generates CS1591:  
  
```  
// CS1591.cs  
// compile with: /W:4 /doc:x.xml  
  
/// text  
public class Test  
{  
   // /// text  
   public static void Main()   // CS1591, remove "//" from previous line  
   {  
   }  
}  
```