---
title: "Compiler Error CS1511"
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
ms.assetid: c04b5268-5bc3-41db-af6b-463ab1d802b4
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1511
Keyword 'base' is not available in a static method  
  
 The [base](../vs140/base--C#-Reference-.md) keyword was used in a [static](../vs140/static--C#-Reference-.md) method. `base` can only be called in an instance constructor, instance method, or instance accessor.  
  
## Example  
 The following sample generates CS1511.  
  
```  
// CS1511.cs  
// compile with: /target:library  
public class A  
{  
   public int j = 0;  
}  
  
class C : A  
{  
   public void Method()  
   {  
      base.j = 3;   // base allowed here  
   }  
  
   public static int StaticMethod()  
   {  
      base.j = 3;   // CS1511  
      return 1;  
   }  
}  
```