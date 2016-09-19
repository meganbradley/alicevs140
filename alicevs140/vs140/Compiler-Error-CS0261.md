---
title: "Compiler Error CS0261"
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
ms.assetid: c2af7b31-4a48-457a-8d9b-0956dd0d46f9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0261
Partial declarations of 'type' must be all classes, all structs, or all interfaces  
  
 This error occurs if a partial type is declared as a different type of construct in various places. For more information, see [Partial Class Definitions (C# Programmer's Reference)](../vs140/Partial-Classes-and-Methods--C#-Programming-Guide-.md).  
  
 The following sample generates CS0261:  
  
```  
// CS0261.cs  
partial class A  // CS0261 – A declared as a class here, but as a struct below  
{  
}  
  
partial struct A  
{  
}  
```