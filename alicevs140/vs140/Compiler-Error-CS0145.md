---
title: "Compiler Error CS0145"
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
ms.assetid: e5f9a90f-1700-4e6a-8f82-23d0c0287b85
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0145
A const field requires a value to be provided  
  
 You must initialize a [const](../vs140/const--C#-Reference-.md) variable. For more information, see [Constants (C# Programmer's Reference)](../Topic/Constants%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0145:  
  
```  
// CS0145.cs  
class MyClass  
{  
   const int i;   // CS0145  
   // try the following line instead  
   // const int i = 0;  
  
   public static void Main()  
   {  
   }  
}  
```