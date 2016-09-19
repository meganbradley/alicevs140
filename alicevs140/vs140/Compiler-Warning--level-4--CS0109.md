---
title: "Compiler Warning (level 4) CS0109"
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
ms.assetid: 42ac72e5-5081-4e8b-b2cf-5e10c1606676
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) CS0109
The member 'member' does not hide an inherited member. The new keyword is not required  
  
 A class declaration included the [new](../vs140/new--C#-Reference-.md) keyword even though the declaration does not override an existing declaration in a base class. You can delete the **new** keyword.  
  
 The following sample generates CS0109:  
  
```  
// CS0109.cs  
// compile with: /W:4  
namespace x  
{  
   public class a  
   {  
      public int i;  
   }  
  
   public class b : a  
   {  
      public new int i;  
      public new int j;   // CS0109  
      public static void Main()  
      {  
      }  
   }  
}  
```