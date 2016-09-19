---
title: "Compiler Warning (level 2) CS0280"
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
ms.assetid: 9b453478-92aa-4fd2-9b87-780fd138603a
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS0280
'type' does not implement the 'pattern name' pattern. 'method name' has the wrong signature.  
  
 Two statements in C#, **foreach** and **using**, rely on predefined patterns, "collection" and "resource" respectively. This warning occurs when the compiler cannot match one of these statements to its pattern due to a method's incorrect signature. For example, the "collection" pattern requires that there be a method called <xref:System.Collections.IEnumerator.MoveNext?qualifyHint=False> which takes no parameters and returns a `boolean`. Your code might contain a <xref:System.Collections.IEnumerator.MoveNext?qualifyHint=False> method that has a parameter or perhaps returns an object.  
  
 The "resource" pattern and `using` provide another example. The "resource" pattern requires the <xref:System.IDisposable.Dispose?qualifyHint=False> method; if you define a property with the same name, you will get this warning.  
  
 To resolve this warning, ensure that the method signatures in your type match the signatures of the corresponding methods in the pattern, and ensure that you have no properties with the same name as a method required by the pattern.  
  
## Example  
 The following sample generates CS0280.  
  
```  
// CS0280.cs  
using System;  
using System.Collections;  
  
public class ValidBase: IEnumerable  
{  
   IEnumerator IEnumerable.GetEnumerator()  
   {  
      yield return 0;  
   }  
  
   internal IEnumerator GetEnumerator()  
   {  
      yield return 0;  
   }  
}  
  
class Derived : ValidBase  
{  
   // field, not method  
   new public int GetEnumerator;  
}  
  
public class Test  
{  
   public static void Main()  
   {  
      foreach (int i in new Derived()) {}   // CS0280  
   }  
}  
```