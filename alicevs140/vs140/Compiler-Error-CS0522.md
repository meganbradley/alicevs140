---
title: "Compiler Error CS0522"
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
ms.assetid: f749f21e-92ee-495c-9b53-179ce9342d05
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0522
'constructor' : structs cannot call base class constructors  
  
 A [struct](../vs140/struct--C#-Reference-.md) cannot call a base class constructor; remove the call to the base class constructor.  
  
 The following sample generates CS0522:  
  
```  
// CS0522.cs  
public class clx  
{  
   public clx(int i)  
   {  
   }  
  
   public static void Main()  
   {  
   }  
}  
  
public struct cly  
{  
   public cly(int i):base(0)   // CS0522  
   // try the following line instead  
   // public cly(int i)  
   {  
   }  
}  
```