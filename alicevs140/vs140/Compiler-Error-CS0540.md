---
title: "Compiler Error CS0540"
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
ms.assetid: 2da2cd4a-0ff1-45ea-bb72-ea078bc95dea
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0540
'interface member' : containing type does not implement interface 'interface'  
  
 You attempted to implement an interface member in a [class](../vs140/class--C#-Reference-.md) that does not derive from the [interface](../vs140/interface--C#-Reference-.md). You should either delete the implementation of the interface member or add the interface to the base-class list of the class.  
  
## Example  
 The following sample generates CS0540.  
  
```  
// CS0540.cs  
interface I  
{  
   void m();  
}  
  
public class Clx  
{  
   void I.m() {}   // CS0540  
}  
  
// OK  
public class Cly : I  
{  
   void I.m() {}  
   public static void Main() {}  
}  
```  
  
## Example  
 The following sample generates CS0540.  
  
```  
// CS0540_b.cs  
using System;  
class C {  
   void IDisposable.Dispose() {}   // CS0540  
}  
  
class D : IDisposable {  
   void IDisposable.Dispose() {}  
   public void Dispose() {}  
  
   static void Main() {  
      using (D d = new D()) {}  
   }  
}  
```