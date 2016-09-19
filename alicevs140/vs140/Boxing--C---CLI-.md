---
title: "Boxing (C++-CLI)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
H1: Boxing (C++/CLI)
ms.assetid: f4ee27a8-6a34-432d-b9ec-39285d513b23
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Boxing (C++-CLI)
Boxing is the process of converting a value type to the type `object` or to any interface type that's implemented by the value type. When the common language runtime (CLR) boxes a value type, it wraps the value in a `System.Object` and stores it on the managed heap. Unboxing extracts the value type from the object. Boxing is implicit; unboxing is explicit.  
  
## Related Articles  
  
|Title|Description|  
|-----------|-----------------|  
|[How to: Explicitly Request Boxing](../vs140/How-to--Explicitly-Request-Boxing.md)|Describes how to explicitly request boxing on a variable.|  
|[How to: Use gcnew to Create Value Types and Use Implicit Boxing](../vs140/How-to--Use-gcnew-to-Create-Value-Types-and-Use-Implicit-Boxing.md)|Shows how to use `gcnew` to create a boxed value type that can be placed on the managed, garbage-collected heap.|  
|[How to: Unbox](../vs140/How-to--Unbox.md)|Shows how to unbox and modify a value.|  
|[Standard Conversions and Implicit Boxing](../vs140/Standard-Conversions-and-Implicit-Boxing.md)|Shows that a standard conversion is chosen by the compiler over a conversion that requires boxing.|  
|[.NET Programming in Visual C++](../vs140/.NET-Programming-with-C---CLI--Visual-C---.md)|The top-level article for .NET programming in the Visual C++ documentation.|