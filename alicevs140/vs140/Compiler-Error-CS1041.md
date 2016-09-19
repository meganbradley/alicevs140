---
title: "Compiler Error CS1041"
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
ms.assetid: 9f62c058-cd28-4cb5-835c-d0f25f4fd08e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1041
Identifier expected, 'keyword' is a keyword  
  
 A reserved word for the C# language was found where an identifier was expected. Replace the [keyword](../Topic/C%23%20Keywords.md) with a user-specified identifier.  
  
## Example  
 The following sample generates CS1041:  
  
```  
// CS1041a.cs  
class MyClass  
{  
    public void f(int long)   // CS1041  
    // Try the following instead:  
    // public void f(int i)  
    {  
    }  
  
    public static void Main()  
    {  
    }  
}  
```  
  
## Example  
 When you are importing from another programming language that does not have the same set of reserved words, you can modify the reserved identifier with the @ prefix, as demonstrated in the following sample.  
  
 An identifier with an `@` prefix is called a verbatim identifier.  
  
```  
// CS1041b.cs  
class MyClass  
{  
    public void f(int long)   // CS1041  
    // Try the following instead:  
    // public void f(int @long)  
    {  
    }  
  
    public static void Main()  
    {  
    }  
}  
```