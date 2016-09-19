---
title: "Compiler Error CS0180"
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
ms.assetid: a21bf0a2-ed5a-4ddd-88d3-240babc5888a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0180
'member' cannot be both extern and abstract  
  
 The [abstract](../vs140/abstract--C#-Reference-.md) and [extern](../Topic/extern%20\(C%23%20Reference\).md) keywords are mutually exclusive. The `extern` keyword means that the member is defined outside the file, and **abstract** means that the implementation is provided in a derived class. For more information, see [Class and Struct Methods (C# Programmer's Reference)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0180:  
  
```  
// CS0180.cs  
namespace MyNamespace  
{  
   public class MyClass  
   {  
      public extern abstract int Foo(int a);   // CS0180  
  
      public static void Main()  
      {  
      }  
   }  
}  
```