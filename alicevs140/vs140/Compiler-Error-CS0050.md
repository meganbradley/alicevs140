---
title: "Compiler Error CS0050"
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
ms.topic: error-reference
ms.assetid: dead2d28-f4db-4afe-b8dd-38968625f7c3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0050
Inconsistent accessibility: return type 'type' is less accessible than method 'method'  
  
 The return type and each of the types referenced in the formal parameter list of a method must be at least as accessible as the method itself. For more information, see [Access Modifiers (C# Programmers Reference)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS0050 because no accessiblity modifier is supplied for `MyClass` and its accessibility therefore defaults to `private`.  
  
```  
// CS0050.cs  
class MyClass //accessibility defaults to private  
// try the following line instead  
// public class MyClass   
{  
}  
  
public class MyClass2  
{  
    public static MyClass MyMethod()   // CS0050  
    {  
        return new MyClass();  
    }  
  
    public static void Main() { }  
}  
```