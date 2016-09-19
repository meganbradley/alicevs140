---
title: "Compiler Warning (level 1) CS0197"
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
ms.assetid: 2b5b1b8d-ce13-4bd7-b80a-abb80e9f79ad
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS0197
Passing 'argument' as ref or out or taking its address may cause a runtime exception because it is a field of a marshal-by-reference class  
  
 Any class that derives, directly or indirectly, from <xref:System.MarshalByRefObject?qualifyHint=False> is a marshal-by-reference class. Such a class can be marshaled by reference across process and machine boundaries. Thus, instances of this class could be proxies to remote objects. You cannot pass a field of a proxy object as [ref](../vs140/ref--C#-Reference-.md) or [out](../vs140/out--C#-Reference-.md). So, you cannot pass fields of such a class as `ref` or `out`, unless the instance is [this](../vs140/this--C#-Reference-.md), which can not be a proxy object.  
  
## Example  
 The following sample generates CS0197.  
  
```  
// CS0197.cs  
// compile with: /W:1  
class X : System.MarshalByRefObject  
{  
   public int i;  
}  
  
class M  
{  
   public int i;  
   static void AddSeventeen(ref int i)  
   {  
      i += 17;  
   }  
  
   static void Main()  
   {  
      X x = new X();  
      x.i = 12;  
      AddSeventeen(ref x.i);   // CS0197  
  
      // OK  
      M m = new M();  
      m.i = 12;  
      AddSeventeen(ref m.i);  
   }  
}  
```