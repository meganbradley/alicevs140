---
title: "Compiler Error CS0158"
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
ms.assetid: 88ac61a9-ce55-4272-9141-0873765a7034
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0158
The label 'label' shadows another label by the same name in a contained scope  
  
 A label in an inner scope hides a label with the same name in an outer scope. For more information, see [goto (C# Programmer's Reference)](../vs140/goto--C#-Reference-.md).  
  
 The following sample generates CS0158:  
  
```  
// CS0158.cs  
namespace MyNamespace  
{  
   public class MyClass  
   {  
      public static void Main()  
      {  
         goto lab1;  
         lab1:  
         {  
            lab1:  
            goto lab1;   // CS0158  
         }  
      }  
   }  
}  
```