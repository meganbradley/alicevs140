---
title: "Compiler Error CS0271"
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
ms.assetid: eadc9fb5-7770-4ec4-94f6-3c7cf37eec06
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0271
The property or indexer 'property/indexer' cannot be used in this context because the get accessor is inaccessible  
  
 This error occurs when you try to access an inaccessible `get` accessor. To resolve this error, increase the accessibility of the accessor, or change the calling location. For more information, see [Accessor Accessibility](../vs140/Restricting-Accessor-Accessibility--C#-Programming-Guide-.md) and [Properties (C# Programmer's Reference)](../vs140/Properties--C#-Programming-Guide-.md).  
  
 The following example generates CS0271:  
  
```  
// CS0271.cs  
public class MyClass  
{  
   public int Property  
   {  
      private get { return 0; }  
      set { }  
   }  
  
   public int Property2  
   {  
      get { return 0; }  
      set { }  
   }  
}  
  
public class Test  
{  
   public static void Main(string[] args)   
   {  
      MyClass c = new MyClass();  
      int a = c.Property;   // CS0271  
      int b = c.Property2;   // OK  
   }  
}  
```