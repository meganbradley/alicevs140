---
title: "Compiler Error CS0153"
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
ms.assetid: 3a0791e9-0ab9-4eaa-a230-d39aabaa9d5d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0153
A goto case is only valid inside a switch statement  
  
 An attempt was made to use [switch](../vs140/switch--C#-Reference-.md) syntax outside of a **switch** statement. For more information, see [switch (C# Programmer's Reference)](../vs140/switch--C#-Reference-.md).  
  
 The following sample generates CS0153:  
  
```  
// CS0153.cs  
public class a  
{  
   public static void Main()  
   {  
      goto case 5;   // CS0153  
   }  
}  
```