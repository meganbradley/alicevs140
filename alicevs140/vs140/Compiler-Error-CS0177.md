---
title: "Compiler Error CS0177"
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
ms.assetid: 852a8c2a-2411-4800-af7c-4c572d9900d3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0177
The out parameter 'parameter' must be assigned to before control leaves the current method  
  
 A parameter marked with the [out](../vs140/out--C#-Reference-.md) keyword was not assigned a value in the method body. For more information, see [Passing Parameters (C# Programmer's Reference)](../vs140/Passing-Parameters--C#-Programming-Guide-.md)  
  
 The following sample generates CS0177:  
  
```  
// CS0177.cs  
public class MyClass  
{  
   public static void Foo(out int i)   // CS0177  
   {  
   // uncomment the following line to resolve this error  
   //   i = 0;  
   }  
  
   public static void Main()  
   {  
       int x = -1;  
       Foo(out x);  
   }  
}  
```