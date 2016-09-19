---
title: "Compiler Error CS1536"
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
ms.assetid: 65f14fbb-df79-4759-8911-93f8f90f5a60
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1536
Invalid parameter type void  
  
 It is not necessary or valid to specify a [void](../vs140/void--C#-Reference-.md) parameter other than a void pointer.  
  
 The following sample generates CS1536:  
  
```  
// CS1536.cs  
class a  
{  
   public static int x( void )   // CS1536  
   // try the following line instead  
   // public static int x()  
   {  
      return 0;  
   }  
  
   public static void Main()  
   {  
   }  
}  
```