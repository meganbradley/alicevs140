---
title: "Compiler Error CS1576"
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
ms.assetid: 3e39cb80-e7de-4c78-a22a-57e267121a96
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1576
The line number specified for #line directive is missing or invalid  
  
 The compiler detected an error with the value passed to the [#line](../vs140/#line--C#-Reference-.md) directive.  
  
 The following sample generates CS1576:  
  
```  
// CS1576.cs  
public class MyClass  
{  
   static void Main()  
   {  
      #line "abc.sc"         // CS1576  
      // try the following line instead  
      //#line  101 "abc.sc"  
      intt i;  // error will be reported on line 101  
   }  
}  
```