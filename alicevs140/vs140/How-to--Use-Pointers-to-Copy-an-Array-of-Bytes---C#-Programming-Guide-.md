---
title: "How to: Use Pointers to Copy an Array of Bytes  (C# Programming Guide)"
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
ms.assetid: ec16fbb4-a24e-45f5-a763-9499d3fabe0a
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use Pointers to Copy an Array of Bytes  (C# Programming Guide)
The following example uses pointers to copy bytes from one array to another.  
  
 This example uses the [unsafe](../vs140/unsafe--C#-Reference-.md) keyword, which enables you to use pointers in the `Copy` method. The [fixed](../vs140/fixed-Statement--C#-Reference-.md) statement is used to declare pointers to the source and destination arrays. This *pins* the location of the source and destination arrays in memory so that they will not be moved by garbage collection. The memory blocks for the arrays are unpinned when the `fixed` block is completed. Because the `Copy` method in this example uses the `unsafe` keyword, it must be compiled with the **/unsafe** compiler option. To set the option in Visual Studio, right-click the project name, and then click **Properties**. On the **Build** tab, select **Allow unsafe code**.  
  
## Example  
 [!CODE [csProgGuidePointers#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#3)]  
  
 [!CODE [csProgGuidePointers#18](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#18)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Unsafe Code and Pointers (C# Programming Guide)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md)   
 [/unsafe (Enable Unsafe Mode)](../Topic/-unsafe%20\(C%23%20Compiler%20Options\).md)   
 [Garbage Collection](assetId:///22b6cb97-0c80-4eeb-a2cf-5ed7655e37f9)