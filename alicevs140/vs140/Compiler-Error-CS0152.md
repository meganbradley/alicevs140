---
title: "Compiler Error CS0152"
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
ms.assetid: 4915ca16-6485-4e1f-ace0-c71a7b339ba4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0152
The label 'label' already occurs in this switch statement  
  
 A label was repeated in a [switch](../vs140/switch--C#-Reference-.md) statement. For more information, see [switch (C# Programmers Reference)](../vs140/switch--C#-Reference-.md).  
  
 The following sample generates CS0152:  
  
```  
// CS0152.cs  
namespace MyNamespace  
{  
   public class MyClass  
   {  
      public static void Main()  
      {  
         int i = 0;  
  
         switch (i)  
         {  
            case 1:  
               i++;  
               return;  
  
            case 1:   // CS0152, two case 1 statements  
               i++;  
               return;  
         }  
      }  
   }  
}  
```