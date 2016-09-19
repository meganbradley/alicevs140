---
title: "Compiler Error CS0594"
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
ms.assetid: a3d6bde1-db63-4c5c-a425-8c6a39e00999
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0594
Floating-point constant is outside the range of type 'type'  
  
 A value was assigned to a floating-point variable that is too large for the variables of this data type. See [Integral Types Table](../vs140/Integral-Types-Table--C#-Reference-.md) for information about the range of values allowed in data types.  
  
 The following sample generates CS0594:  
  
```  
// CS0594.cs  
namespace MyNamespace  
{  
   public class MyClass  
   {  
      public static void Main()  
      {  
         float f = 6.77777777777E400;   // CS0594, value too large  
      }  
   }  
}  
```