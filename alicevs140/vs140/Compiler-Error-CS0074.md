---
title: "Compiler Error CS0074"
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
ms.assetid: 9395c532-3934-4553-8e41-042bfe3399ce
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0074
'event': abstract event cannot have initializer  
  
 If an [event](../Topic/event%20\(C%23%20Reference\).md) is marked as **abstract**, it cannot be initialized. For more information, see [Events (C# Programmer's Reference)](../Topic/Events%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0074:  
  
```  
// CS0074.cs  
delegate void D();  
  
abstract class Test  
{  
   public abstract event D e = null;   // CS0074  
   // try the following line instead  
   // public abstract event D e;  
  
   public static void Main()  
   {  
   }  
}  
```