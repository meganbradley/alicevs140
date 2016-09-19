---
title: "Compiler Error CS1012"
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
ms.assetid: 4acc5fe0-da47-4882-b7d8-557767d7cf03
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1012
Too many characters in character literal  
  
 An attempt was made to initialize a [char](../vs140/char--C#-Reference-.md) constant with more than one character.  
  
 CS1012 can also occur when doing data binding. For example the following line will give an error:  
  
 `<%# DataBinder.Eval(Container.DataItem, 'doctitle') %>`  
  
 Try the following line instead:  
  
 `<%# DataBinder.Eval(Container.DataItem, "doctitle") %>`  
  
 The following sample generates CS1012:  
  
```  
// CS1012.cs  
class Sample  
{  
   static void Main()  
   {  
      char a = 'xx';   // CS1012  
      char a2 = 'x';   // OK  
      System.Console.WriteLine(a2);  
   }  
}  
```