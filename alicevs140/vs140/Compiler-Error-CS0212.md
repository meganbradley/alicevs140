---
title: "Compiler Error CS0212"
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
ms.assetid: 1b8973b8-03c9-42a6-bf61-2e401b89387e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0212
You can only take the address of an unfixed expression inside of a fixed statement initializer  
  
 For more information, see [Unsafe Code and Pointers (C# Programmer's Reference)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md).  
  
 The following sample shows how to take the address of an unfixed expression. The following sample generates CS0212.  
  
```  
// CS0212a.cs  
// compile with: /unsafe /target:library  
  
public class A {  
   public int iField = 5;  
  
   unsafe public void M() {   
      A a = new A();  
      int* ptr = &a.iField;   // CS0212   
   }  
  
   // OK  
   unsafe public void M2() {  
      A a = new A();  
      fixed (int* ptr = &a.iField) {}  
   }  
}  
```  
  
 The following sample also generates CS0212 and shows how to resolve the error:  
  
```  
// CS0212b.cs  
// compile with: /unsafe /target:library  
using System;  
  
public class MyClass  
{  
   unsafe public void M()  
   {  
      // Null-terminated ASCII characters in an sbyte array   
      sbyte[] sbArr1 = new sbyte[] { 0x41, 0x42, 0x43, 0x00 };  
      sbyte* pAsciiUpper = &sbArr1[0];   // CS0212  
      // To resolve this error, delete the previous line and   
      // uncomment the following code:  
      // fixed (sbyte* pAsciiUpper = sbArr1)  
      // {  
      //    String szAsciiUpper = new String(pAsciiUpper);  
      // }  
   }  
}  
```