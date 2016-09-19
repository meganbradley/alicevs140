---
title: "Compiler Error CS0621"
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
ms.assetid: 7ff392c6-478c-4971-93dc-f837b1b8748c
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0621
'member' : virtual or abstract members cannot be private  
  
 Private **virtual** or **abstract** members are not allowed.  
  
 The following sample generates CS0621:  
  
```  
// CS0621.cs  
abstract class MyClass  
{  
   private virtual void DoNothing1()   // CS0621  
   {  
   }  
  
   private abstract void DoNothing2();   // CS0621  
  
   public static void Main()  
   {  
   }  
}  
```