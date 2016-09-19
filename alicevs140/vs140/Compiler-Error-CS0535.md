---
title: "Compiler Error CS0535"
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
ms.assetid: 282ed5d6-acb7-445b-999f-27a973ccc0b5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0535
'class' does not implement interface member 'member'  
  
 A [class](../vs140/class--C#-Reference-.md) derived from an [interface](../vs140/interface--C#-Reference-.md), but the class did not implement one or more of the interface's members. A class must implement all members of interfaces from which it derives or else be declared `abstract`.  
  
## Example  
 The following sample generates CS0535.  
  
```  
// CS0535.cs  
public interface A  
{  
   void F();  
}  
  
public class B : A {}   // CS0535 A::F is not implemented  
  
// OK  
public class C : A {  
   public void F() {}  
   public static void Main() {}  
}  
```  
  
## Example  
 The following sample generates CS0535.  
  
```  
// CS0535_b.cs  
using System;  
class C : IDisposable {}   // CS0535  
  
// OK  
class D : IDisposable {  
   void IDisposable.Dispose() {}  
   public void Dispose() {}  
  
   static void Main() {  
      using (D d = new D()) {}  
   }  
}  
```