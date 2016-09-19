---
title: "Compiler Error CS0663"
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
ms.assetid: 9f96c42b-dcc8-4a0f-8404-289fc88dba5e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0663
Cannot define overloaded methods that differ only on ref and out.  
  
 Methods that differ only on their use of [ref](../vs140/ref--C#-Reference-.md) and [out](../vs140/out--C#-Reference-.md) on a parameter are not allowed.  
  
 The following sample generates CS0663:  
  
```  
// CS0663.cs  
class TestClass  
{  
   public static void Main()  
   {  
   }  
  
   public void Test(ref int i)  
   {  
   }  
  
   public void Test(out int i)   // CS0663  
   {  
   }  
}  
```