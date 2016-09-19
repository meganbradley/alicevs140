---
title: "Compiler Error CS0079"
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
ms.assetid: 71c85883-b72f-402f-a828-18ca92976273
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0079
The event 'event' can only appear on the left hand side of += or -=  
  
 An [event](../Topic/event%20\(C%23%20Reference\).md) was called incorrectly. For more information, see [Events (C# Programmer's Reference)](../Topic/Events%20\(C%23%20Programming%20Guide\).md) and [Delegates (C# Programmer's Reference)](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0079:  
  
```  
// CS0079.cs  
using System;  
  
public delegate void MyEventHandler();  
  
public class Class1  
{  
   private MyEventHandler _e;  
  
   public event MyEventHandler Pow  
   {  
      add  
      {  
         _e += value;  
         Console.WriteLine("in add accessor");  
      }  
      remove  
      {  
         _e -= value;  
         Console.WriteLine("in remove accessor");  
      }  
   }  
  
   public void Handler()  
   {  
   }  
  
   public void Fire()  
   {  
      if (_e != null)  
      {  
         Pow();   // CS0079  
         // try the following line instead  
         // _e();  
      }  
   }  
  
   public static void Main()  
   {  
      Class1 p = new Class1();  
      p.Pow += new MyEventHandler(p.Handler);  
      p._e();  
      p.Pow += new MyEventHandler(p.Handler);  
      p._e();  
      p._e -= new MyEventHandler(p.Handler);  
      if (p._e != null)  
      {  
         p._e();  
      }  
      p.Pow -= new MyEventHandler(p.Handler);  
      if (p._e != null)  
      {  
         p._e();  
      }  
   }  
}  
```