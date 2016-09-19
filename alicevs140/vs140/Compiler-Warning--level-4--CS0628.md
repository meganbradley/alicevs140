---
title: "Compiler Warning (level 4) CS0628"
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
ms.assetid: a54cfad8-27c9-4abb-8c83-982615489a10
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) CS0628
'member' : new protected member declared in sealed class  
  
 A [sealed](../vs140/sealed--C#-Reference-.md) class cannot introduce a [protected](../vs140/protected--C#-Reference-.md) member because no other class will be able to inherit from the `sealed` class and use the `protected` member.  
  
 The following sample generates CS0628:  
  
```  
// CS0628.cs  
// compile with: /W:4  
sealed class C  
{  
   protected int i;   // CS0628  
}  
  
class MyClass  
{  
   public static void Main()  
   {  
   }  
}  
```