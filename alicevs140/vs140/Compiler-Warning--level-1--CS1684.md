---
title: "Compiler Warning (level 1) CS1684"
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
ms.assetid: 620419bf-b6d5-4cda-a549-fcacf2f08920
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1684
Reference to type 'Type Name' claims it is defined in 'Namespace', but it could not be found  
  
 This error can be caused by a reference inside one namespace referring to a type that it says exists inside a second namespace, but the type does not exist. For example, mydll.dll says that type `A` exists inside yourdll.dll, but no such type exists inside yourdll.dll. One possible cause of this error is that the version of yourdll.dll you are using is too old and `A` has not yet been defined.  
  
 The following sample generates CS1684.  
  
## Example  
  
```  
// CS1684_a.cs  
// compile with: /target:library /keyfile:CS1684.key  
public class A {  
   public void Test() {}  
}  
  
public class C2 {}  
```  
  
## Example  
  
```  
// CS1684_b.cs  
// compile with: /target:library /r:cs1684_a.dll  
// post-build command: del /f CS1684_a.dll  
using System;  
public class Ref   
{  
   public static A GetA() { return new A(); }  
   public static C2 GetC() { return new C2(); }  
}  
```  
  
## Example  
 We now rebuild the first assembly, leaving out the definition of the class C2 not to be defined in the recompilation.  
  
```  
// CS1684_c.cs  
// compile with: /target:library /keyfile:CS1684.key /out:CS1684_a.dll  
public class A {  
   public void Test() {}  
}  
```  
  
## Example  
 This module references the second module by means of the identifier `Ref`. But the second module contains a reference to the class `C2`, which no longer exists because of the compilation in the previous step, and therefore the CS1684 error message is returned from the compilation of this module.  
  
```  
// CS1684_d.cs  
// compile with: /reference:cs1684_a.dll /reference:cs1684_b.dll  
// CS1684 expected  
class Tester  
{  
   public static void Main()  
   {  
      Ref.GetA().Test();  
   }  
}  
```