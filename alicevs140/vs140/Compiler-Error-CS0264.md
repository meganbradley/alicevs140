---
title: "Compiler Error CS0264"
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
ms.assetid: a8a87185-5915-4b0d-a8cd-2f129ea51b8f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0264
Partial declarations of 'type' must have the same type parameter names in the same order  
  
 This error occurs if you are defining a generic type in partial declarations and the type parameters are not consistent in name or order throughout all of the partial declarations. To get rid of this error, check the type parameters for each partial declaration and make sure the same name and order of parameters is used. For more information, see [Partial Class Definitions (C# Programmer's Reference)](../vs140/Partial-Classes-and-Methods--C#-Programming-Guide-.md).and [Generic Type Parameters (C# Programmers Reference)](../Topic/Generic%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following example generates CS0264.  
  
```  
// CS0264.cs  
  
partial class MyClass<T>  // CS0264  
{  
}  
  
partial class MyClass <MyType>  
{  
}  
```