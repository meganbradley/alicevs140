---
title: "Compiler Error CS0526"
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
ms.assetid: befc46b4-28ea-40d3-89ac-132b92455772
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0526
Interfaces cannot contain constructors  
  
 Constructors cannot be defined for [interfaces](../vs140/interface--C#-Reference-.md). A method is considered a constructor if it has the same name as the class and no return type.  
  
 The following sample generates CS0526:  
  
```  
// CS0526.cs  
namespace x  
{  
   public interface clx  
   {  
      public clx()   // CS0526  
      {  
      }  
   }  
  
   public class cly  
   {  
      public static void Main()  
      {  
      }  
   }  
}  
```