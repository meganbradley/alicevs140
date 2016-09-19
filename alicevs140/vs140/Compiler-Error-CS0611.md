---
title: "Compiler Error CS0611"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bbd857a0-9454-4438-a21c-fef5bc7eee06
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0611
Array elements cannot be of type 'type'  
  
 There are some types that cannot be used as the type of an array. These types include **System.TypedReference** and **System.ArgIterator**.  
  
 The following sample generates CS0611 as a result of using **System.TypedReference** as an array element:  
  
```  
// CS0611.cs  
public class a  
{  
   public static void Main()  
   {  
      System.TypedReference[] ao = new System.TypedReference [10];   // CS0611  
      // try the following line instead  
      // int[] ao = new int[10];  
   }  
}  
```