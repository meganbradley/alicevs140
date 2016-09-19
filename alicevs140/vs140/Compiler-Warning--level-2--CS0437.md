---
title: "Compiler Warning (level 2) CS0437"
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
ms.assetid: cba5c9b6-a0bc-4f19-b1f0-c1f66436ee91
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS0437
The type 'type' in 'assembly2' conflicts with the imported namespace 'namespace' in 'fassembly1'. Using the type defined in 'assembly'.  
  
 This warning is issued when a type in a source file, file_2, conflicts with an imported namespace in file _1. The compiler uses the type in the source file.  
  
## Example  
  
```  
// CS0437_a.cs  
// compile with: /target:library  
namespace Util   
{  
   public class A {  
      public void Test() {  
         System.Console.WriteLine("CS0437_a.cs");  
      }  
   }  
}  
```  
  
## Example  
 The following sample generates CS0437.  
  
```  
// CS0437_b.cs  
// compile with: /reference:CS0437_a.dll /W:2  
// CS0437 expected  
class Util   
{  
   public class A {   
      public void Test() {  
         System.Console.WriteLine("CS0437_b.cs");  
      }  
   }  
}  
  
public class Test   
{  
   public static void Main()   
   {  
      Util.A x = new Util.A();  
      x.Test();  
   }  
}  
```