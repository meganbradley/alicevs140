---
title: "Compiler Error CS0515"
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
ms.assetid: 0f8c0253-218d-4c21-b22c-fa5802ba4e7f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0515
'function' : access modifiers are not allowed on static constructors  
  
 A static constructor cannot have an [access modifier](../vs140/Modifiers--C#-Reference-.md).  
  
## Example  
 The following sample generates CS0515:  
  
```  
// CS0515.cs  
public class Clx  
{  
    public static void Main()  
    {  
    }  
}  
  
public class Clz  
{  
    public static Clz()   // CS0515, remove public keyword  
    {  
    }  
}  
```