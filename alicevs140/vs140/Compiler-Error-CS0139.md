---
title: "Compiler Error CS0139"
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
ms.assetid: 235ba3d4-566c-4ef6-801a-a338f4f2a12d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0139
No enclosing loop out of which to break or continue  
  
 A break or continue statement was encountered outside of a loop.  
  
 For more information, see [Jump Statements](../vs140/Jump-Statements--C#-Reference-.md).  
  
 The following sample generates CS0139 twice:  
  
```  
// CS0139.cs  
namespace x  
{  
   public class a  
   {  
      public static void Main()  
      {  
         continue;  // CS0139  
         break;     // CS0139  
      }  
   }  
}  
```