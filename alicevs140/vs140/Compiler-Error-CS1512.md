---
title: "Compiler Error CS1512"
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
ms.assetid: 50740d85-598d-478f-bfe3-e8c2e1a02ab8
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1512
Keyword 'base' is not available in the current context  
  
 The [base](../vs140/base--C#-Reference-.md) keyword was used outside of a method, property, or constructor.  
  
 The following example generates CS1512:  
  
```  
// CS1512.cs  
using System;  
  
class Base {}  
  
class CMyClass : Base  
{  
    private String xx = base.ToString();   // CS1512  
    // Try putting this initialization in the constructor instead:  
    // public CMyClass()  
    // {  
    //    xx = base.ToString();  
    // }  
  
    public static void Main()  
    {  
        CMyClass z = new CMyClass();  
    }  
}  
```