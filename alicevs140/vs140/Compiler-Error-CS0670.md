---
title: "Compiler Error CS0670"
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
ms.assetid: 59379171-284f-4d55-8741-af6a97879abc
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0670
Field cannot have void type  
  
 A field was declared to be of type [void](../vs140/void--C#-Reference-.md).  
  
 The following sample generates CS0670:  
  
```  
// CS0670.cs  
class C  
{  
   void f;   // CS0670  
   // try the following line instead  
   // public int f;  
  
   public static void Main()  
   {  
      C myc = new C();  
      myc.f = 0;  
   }  
}  
```