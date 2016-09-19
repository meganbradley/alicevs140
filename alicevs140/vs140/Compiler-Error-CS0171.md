---
title: "Compiler Error CS0171"
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
ms.assetid: 8c1d76c9-1048-4579-9031-23e3566e6288
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0171
Backing field for automatically implemented property 'name' must be fully assigned before control is returned to the caller. Consider calling the default constructor from a constructor initializer.  
  
 A constructor in a [struct](../vs140/struct--C#-Reference-.md) must initialize all fields in the struct. For more information, see [Constructors (C# Programmer's Reference)](../vs140/Constructors--C#-Programming-Guide-.md).  
  
 The following sample generates CS0171:  
  
```  
// CS0171.cs  
struct MyStruct  
{  
   MyStruct(int initField)   // CS0171  
   {  
      // i = initField;      // uncomment this line to resolve this error  
   }  
   public int i;  
}  
  
class MyClass  
{  
   public static void Main()  
   {  
      MyStruct aStruct = new MyStruct();  
   }  
}  
```