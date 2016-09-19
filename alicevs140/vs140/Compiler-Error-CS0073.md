---
title: "Compiler Error CS0073"
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
ms.assetid: 579ae534-59ab-4fc5-ad7e-f87639f3f9cd
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0073
An add or remove accessor must have a body  
  
 An **add** or **remove** keyword in an [event](../Topic/event%20\(C%23%20Reference\).md) definition must have a body. For more information, see [Events (C# Programmers Reference)](../Topic/Events%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0073:  
  
```  
// CS0073.cs  
delegate void del();  
  
class Test  
{  
   public event del MyEvent  
   {  
      add;   // CS0073  
      // try the following lines instead  
      // add  
      // {  
      //    MyEvent += value;  
      // }  
      remove  
      {  
         MyEvent -= value;  
      }  
  
   }  
  
   public static void Main()  
   {  
   }  
}  
```