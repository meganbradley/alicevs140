---
title: "Compiler Error CS0610"
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
ms.assetid: 6cdce74c-5c00-4539-9df1-32be70e9912d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0610
Field or property cannot be of type 'type'  
  
 There are some types that cannot be used as fields or properties. These types include **System.ArgIterator** and **System.TypedReference**.  
  
 The following sample generates CS0610 as a result of using **System.TypedReference** as a field:  
  
```  
// CS0610.cs  
public class MainClass  
{  
   System.TypedReference i;   // CS0610  
   public static void Main ()  
   {  
   }  
  
   public static void Test(System.TypedReference i)   // OK  
   {  
   }  
}  
```