---
title: "Compiler Error CS0038"
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
ms.assetid: ed378c79-c31b-4373-adfa-ee5dd2dccc9e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0038
Cannot access a nonstatic member of outer type 'type1' via nested type 'type2'  
  
 A field in a class is not automatically available to a nested class. To be available to a nested class, the field must be [static](../vs140/static--C#-Reference-.md). Otherwise, you must create an instance of the outer class. For more information, see [Nested Types (C# Programmers Reference)](../vs140/Nested-Types--C#-Programming-Guide-.md).  
  
 The following sample generates CS0038:  
  
```  
// CS0038.cs  
class OuterClass  
{  
   public int count;  
   // try the following line instead  
   // public static int count;  
  
   class InnerClass  
   {  
      void func()  
      {  
         // or, create an instance  
         // OuterClass class_inst = new OuterClass();  
         // int count2 = class_inst.count;  
         int count2 = count;   // CS0038  
      }  
   }  
  
   public static void Main()  
   {  
   }  
}  
```