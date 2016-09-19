---
title: "Compiler Error CS1103"
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
ms.assetid: 513a26ea-9d66-4dc3-b3e6-d709c3089b1a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1103
The first parameter of an extension method cannot be of type 'type'.  
  
 The first parameter of an extension method cannot be a pointer type.  
  
## Example  
 The following example generates CS1103:  
  
```  
// cs1103.cs  
public static class Extensions  
{  
    public unsafe static char* Test(this char* charP) { return charP; } // CS1103  
}   
```  
  
## See Also  
 [Extension Methods (C# Programming Guide)](../Topic/Extension%20Methods%20\(C%23%20Programming%20Guide\).md)   
 [unsafe (C# Reference)](../vs140/unsafe--C#-Reference-.md)