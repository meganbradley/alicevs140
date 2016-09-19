---
title: "Compiler Error CS0500"
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
ms.assetid: b1a45708-702b-482c-bd71-c0c2531e29f3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0500
'class member' cannot declare a body because it is marked abstract  
  
 An [abstract](../vs140/abstract--C#-Reference-.md) method cannot contain its implementation.  
  
 The following sample generates CS0500:  
  
```  
// CS0500.cs  
namespace x  
{  
   abstract public class clx  
   {  
      abstract public void f(){}   // CS0500  
      // try the following line instead  
      // abstract public void f();  
   }  
  
   public class cly  
   {  
      public static int Main()  
      {  
         return 0;  
      }  
   }  
}  
```