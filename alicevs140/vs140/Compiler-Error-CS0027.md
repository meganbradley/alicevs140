---
title: "Compiler Error CS0027"
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
ms.assetid: 3a599876-9643-4c68-9457-3306858a73e9
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0027
Keyword 'this' is not available in the current context  
  
 The [this](../vs140/this--C#-Reference-.md) keyword was found outside of a property, method, or constructor.  
  
 To fix this error, either modify the statement to eliminate use of the `this` keyword, and/or move part or all of the statement inside a property, method, or constructor.  
  
 The following example generates CS0027:  
  
```  
using System;  
using System.Collections.Generic;  
using System.Text;  
  
namespace ConsoleApplication3  
{  
    class MyClass  
    {  
  
        int err1 = this.Fun() + 1;  // CS0027   
  
        public int Fun()  
        {  
            return 10;  
        }  
  
        public void Test()  
        {  
            // valid use of this  
            int err = this.Fun() + 1;  
            Console.WriteLine(err);  
        }  
  
        public static void Main()  
        {  
            MyClass c = new MyClass();  
            c.Test();  
        }  
    }  
}  
```