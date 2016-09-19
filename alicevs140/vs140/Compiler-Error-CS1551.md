---
title: "Compiler Error CS1551"
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
ms.assetid: 09fde2a2-7466-418a-88ef-395321358b07
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1551
Indexers must have at least one parameter  
  
 An [indexer](../vs140/Indexers--C#-Programming-Guide-.md) that takes no arguments was declared.  
  
 The following sample generates CS1551:  
  
```  
// CS1551.cs  
public class MyClass  
{  
   int intI;  
  
   int this[]   // CS1551  
   // try the following line instead  
   // int this[int i]  
   {  
      get  
      {  
         return intI;  
      }  
      set  
      {  
         intI = value;  
      }  
   }  
  
   public static void Main()  
   {  
   }  
}  
```