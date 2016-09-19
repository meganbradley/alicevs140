---
title: "Compiler Error CS1725"
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
ms.assetid: baef9ae3-b036-41d6-972c-9f3cdae1e8bd
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1725
Friend assembly reference 'reference' is invalid. InternalsVisibleTo declarations cannot have a version, culture, public key token, or processor architecture specified.  
  
 You cannot add a version culture in a friend assembly reference. Partial classes should be visible to friend assemblies.  
  
## Example  
 The following sample generates CS1725.  
  
```  
// CS1725.cs  
// compile with: /target:library  
using System.Runtime.CompilerServices;  
[assembly:InternalsVisibleTo("partial01,version=1.1.0.0")]   // CS1725  
// try the following line instead  
// [assembly:InternalsVisibleTo("partial01")]  
  
partial class TestClass   
{  
   public static string strBar = "my string";  
}  
```  
  
## See Also  
 [How to: Create Signed Friend Assemblies (C# and Visual Basic)](../vs140/How-to--Create-Signed-Friend-Assemblies--C#-and-Visual-Basic-.md)