---
title: "Compiler Error CS0432"
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
ms.assetid: 39b63146-ecb2-4b7a-b3cb-f68fff5069f6
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0432
Alias 'identifier' not found  
  
 This error occurs when you use "::" to the right of an identifier that is not an alias. To resolve the error, use "." instead.  
  
 The following example generates CS0432:  
  
```  
// CS0432.cs  
namespace A {  
    public class B {  
        public static void Meth() { }  
    }  
}  
  
public class Test  
{  
    public static void Main()  
    {  
        A::B.Meth();   // CS0432  
       // To resolve, use the following line instead:  
       // A.B.Meth();  
    }  
}  
```