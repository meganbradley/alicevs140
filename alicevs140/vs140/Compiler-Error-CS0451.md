---
title: "Compiler Error CS0451"
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
ms.assetid: e73544f8-856b-4a92-90e0-dd6cb9d688b1
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0451
The 'new()' constraint cannot be used with the 'struct' constraint  
  
 When specifying constraints on the type of a generic, the `new()` constraint may only be used with class type constraints, interface type constraints, reference type constraints, and type parameter constraints, but not with value type constraints.  
  
## Example  
 The following sample generates CS0451.  
  
```  
// CS0451.cs  
using System;  
public class C4   
{  
   public void F4<T>() where T : struct, new() {}   // CS0451  
}  
  
// OK  
public class C5  
{  
   public void F5<T>() where T : struct {}  
}  
  
public class C6  
{  
   public void F6<T>() where T : new() {}  
}  
  
```