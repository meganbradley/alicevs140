---
title: "Compiler Error CS0531"
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
ms.assetid: 54c2a98b-84e3-481a-a934-7cd6dffa7677
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0531
'member' : interface members cannot have a definition  
  
 Methods that are declared in an [interface](../vs140/interface--C#-Reference-.md) must be implemented in a class that inherits from it and not in the interface itself.  
  
 The following sample generates CS0531:  
  
```  
// CS0531.cs  
namespace x  
{  
   public interface clx  
   {  
      int xclx()   // CS0531, cannot define xclx  
      // Try the following declaration instead:  
      // int xclx();  
      {  
         return 0;  
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