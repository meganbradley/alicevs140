---
title: "Compiler Error CS0452"
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
ms.assetid: 50a87734-fe07-4bce-891d-a76e131db6cc
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0452
The type 'type name' must be a reference type in order to use it as parameter 'parameter name' in the generic type or method 'identifier of generic'  
  
 This error occurs when you pass a value type such as a `struct` or `int` as a parameter to a generic type or method that has a reference type constraint.  
  
## Example  
 The following code generates error CS0452.  
  
```  
// CS0452.cs  
using System;  
public class BaseClass<S> where S : class { }  
public class Derived1 : BaseClass<int> { } // CS0452  
public class Derived2<S> : BaseClass<S> where S : struct { } // CS0452  
```  
  
## See Also  
 [Constraints on Type Parameters (C# Programming Guide)](../Topic/Constraints%20on%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md)