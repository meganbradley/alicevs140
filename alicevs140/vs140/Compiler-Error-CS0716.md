---
title: "Compiler Error CS0716"
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
ms.assetid: 806d25ef-f8a7-4c94-823e-e07904defcf4
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0716
Cannot convert to static type 'type'  
  
 This error occurs if your code uses a cast to convert to a static type. Since it is not possible for an object to be an instance of a static type, casting to a static type can never be a meaningful cast.  
  
## Example  
 The following sample generates CS0716:  
  
```  
// CS0716.cs  
  
public static class SC  
{  
    static void F() { }  
}  
  
public class Test  
{  
    public static void Main()  
    {  
        object o = new object();  
        System.Console.WriteLine((SC)o);  // CS0716  
    }  
}  
```