---
title: "Compiler Error CS0134"
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
ms.assetid: c7b57de2-42ad-473e-8e45-8ac7a0caea9a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0134
'variable' is of type 'type'. A const field of a reference type other than string can only be initialized with null.  
  
 A constant-expression is an expression that can be fully evaluated at compile-time. Because the only way to create a non-null value of a reference-type is to apply the new operator, and because the new operator is not permitted in a constant-expression, the only possible value for constants of reference-types other than string is null.  
  
 If you encounter this error by trying to create a [const](../vs140/const--C#-Reference-.md) string array, the solution is to make the array [readonly](../vs140/readonly--C#-Reference-.md), and initialize it in the constructor.  
  
## Example  
 The following example generates CS0134.  
  
```  
// CS0134.cs  
// compile with: /target:library  
class MyTest {}   
  
class MyClass  
{  
   const MyTest test = new MyTest();   // CS0134  
  
   //OK  
   const MyTest test2 = null;  
   const System.String test3 = "test";  
}  
```