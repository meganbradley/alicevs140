---
title: "Compiler Error CS0413"
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
ms.topic: error-reference
ms.assetid: a01bd1ec-015b-433b-be55-b91db268d6a5
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0413
The type parameter 'type parameter' cannot be used with the 'as' operator because it does not have a class type constraint nor a 'class' constraint  
  
 This error occurs if a generic type uses the [as](../vs140/as--C#-Reference-.md) operator, but that generic type does not have a class type constraint. The `as` operator is only allowed with reference types, so the type parameter must be constrained to guarantee that it is not a value type. To avoid this error, use a class type constraint or a reference type constraint.  
  
 This is because the `as` operator could return `null`, which is not a possible value for a value type, and the type parameter must be treated as a value type unless it is a class type constraint or a reference type constraint.  
  
## Example  
 The following sample generates CS0413.  
  
```  
// CS0413.cs  
// compile with: /target:library  
class A {}  
class B : A {}  
  
class CMain  
{  
   A a = null;  
   public void G<T>()  
   {  
      a = new A();  
      System.Console.WriteLine (a as T);  // CS0413  
   }  
  
   // OK  
   public void H<T>() where T : A  
   {  
      a = new A();  
      System.Console.WriteLine (a as T);  
   }  
}  
```