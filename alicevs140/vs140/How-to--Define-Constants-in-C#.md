---
title: "How to: Define Constants in C#"
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
ms.assetid: 43f511be-346c-4b8a-995e-aded94542ece
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Define Constants in C#
Constants are fields whose values are set at compile time and can never be changed. Use constants to provide meaningful names instead of numeric literals ("magic numbers") for special values.  
  
> [!NOTE]
>  In C# the [#define](../vs140/#define--C#-Reference-.md) preprocessor directive cannot be used to define constants in the way that is typically used in C and C++.  
  
 To define constant values of integral types (`int`, `byte`, and so on) use an enumerated type. For more information, see [enum (C# Reference)](../Topic/enum%20\(C%23%20Reference\).md).  
  
 To define non-integral constants, one approach is to group them in a single static class named `Constants`. This will require that all references to the constants be prefaced with the class name, as shown in the following example.  
  
## Example  
 [!CODE [csProgGuideObjects#89](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#89)]  
  
 The use of the class name qualifier helps ensure that you and others who use the constant understand that it is constant and cannot be modified.  
  
## See Also  
 [Objects, Classes and Structs (C# Programming Guide)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)