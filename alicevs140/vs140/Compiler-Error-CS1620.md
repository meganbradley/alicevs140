---
title: "Compiler Error CS1620"
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
ms.assetid: 13933976-218a-4fe2-8fde-5b9af522e2e5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1620
Argument 'number' must be passed with the 'keyword' keyword  
  
 This error occurs if you are passing an argument to a function that takes a [ref](../vs140/ref--C#-Reference-.md) or [out](../vs140/out--C#-Reference-.md) parameter and you don't include the `ref` or `out` keyword at the point of call, or you include the wrong keyword. The error text indicates the appropriate keyword to use and which argument caused the failure.  
  
 The following sample generates CS1620:  
  
```  
// CS1620.cs  
class C  
{  
    void f(ref int i) {}  
    public static void Main()  
    {  
        int x = 1;  
        f(out x);  // CS1620 – f takes a ref parameter, not an out parameter  
        // Try this line instead:  
        // f(ref x);  
    }  
}  
```