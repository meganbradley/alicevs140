---
title: "Compiler Error CS0507"
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
ms.assetid: ddbdb94c-38c3-4022-8d1c-68971d398b87
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0507
'function1' : cannot change access modifiers when overriding 'access' inherited member 'function2'  
  
 An attempt was made to change the access specification in a method override.  
  
## Example  
 The following sample generates CS0507.  
  
```  
// CS0507.cs  
abstract public class clx  
{  
   virtual protected void f() {}  
}  
  
public class cly : clx  
{  
   public override void f() {}   // CS0507  
   public static void Main() {}  
}  
```  
  
## Example  
 CS0507 can also occur if a class attempts to override a method marked as `protected internal` defined in referenced metadata. In this situation, the overriding method should be marked as `protected`.  
  
```  
// CS0507_b.cs  
// compile with: /target:library  
abstract public class clx  
{  
   virtual protected internal void f() {}  
}  
```  
  
## Example  
 The following sample generates CS0507.  
  
```  
// CS0507_c.cs  
// compile with: /reference:cs0507_b.dll  
public class cly : clx  
{  
   protected internal override void f() {}   // CS0507  
   // try the following line instead  
   // protected override void f() {}   // OK  
  
   public static void Main() {}  
}  
```