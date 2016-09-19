---
title: "Compiler Error CS0711"
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
ms.assetid: 3a5a6d90-e15d-4808-a7a6-c85fd011a0d0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0711
Static classes cannot contain destructors  
  
 A static class cannot be instantiated, hence it has no need for constructors or destructors. To avoid this error, remove any destructors from static classes, or, if you really want to construct and destroy instances, make the class non-static.  
  
 The following sample generates CS0711:  
  
```  
// CS0711.cs  
public static class C  
{  
   ~C()  // CS0711  
   {  
   }  
  
   public static void Main()  
   {  
   }  
}  
```