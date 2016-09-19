---
title: "Compiler Error CS1055"
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
ms.assetid: a93cb577-95fc-490a-97c4-2f366409f2c3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1055
An add or remove accessor expected  
  
 If your [event](../Topic/event%20\(C%23%20Reference\).md) is not declared as a field, it must define both **add** and **remove** accessor functions.  
  
 The following sample generates CS1055:  
  
```  
// CS1055.cs  
delegate void del();  
class Test  
{  
   public event del MyEvent  
   {  
      int i;   // CS1055  
      // uncomment accessors and delete previous line to resolve  
      // add  
      // {  
      //    MyEvent += value;  
      // }  
      // remove  
      // {  
      //    MyEvent -= value;  
      // }  
   }  
  
   public static void Main()  
   {  
   }  
}  
```