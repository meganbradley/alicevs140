---
title: "Compiler Error CS0144"
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
ms.assetid: 3904cab1-05bd-44ec-81d0-e36c5656f742
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0144
Cannot create an instance of the abstract class or interface 'interface'  
  
 You cannot create an instance of an [abstract](../vs140/abstract--C#-Reference-.md) class or an [interface](../vs140/interface--C#-Reference-.md). For more information, see [Interfaces (C# Programmer's Reference)](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0144:  
  
```  
// CS0144.cs  
interface MyInterface  
{  
}  
public class MyClass  
{  
   public static void Main()  
   {  
      MyInterface myInterface = new MyInterface ();   // CS0144  
   }  
}  
```