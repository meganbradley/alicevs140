---
title: "Compiler Error CS0717"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1976e82a-d048-4f13-a95a-a7f4e3cd7038
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0717
'static class': static classes cannot be used as constraints  
  
 Static classes cannot be extended as they only contain static members and not instance members. Because they cannot be extended, this makes them useless as type parameters and constraints, as no type can exist that is a specialization of a static class.  
  
## Example  
 The following sample generates CS0717:  
  
```  
// CS0717.cs  
  
public static class SC  
{  
    public static void F()  
    {  
    }  
}  
  
public class G<T> where T : SC  // CS0717  
{  
    public static void Main()  
    {  
    }  
}  
```