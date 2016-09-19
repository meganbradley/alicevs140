---
title: "Compiler Error CS0673"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5921cc27-c0ff-43be-8044-b454c8631c86
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0673
System.Void cannot be used from C# -- use typeof(void) to get the void type object.  
  
 **System.Void** cannot be used in C#.  
  
 The following sample generates CS0673:  
  
```  
// CS0673.cs  
class MyClass  
{  
   public static void Main()  
   {  
      System.Type t = typeof(System.Void);   // CS0673  
      // try the following line instead  
      // System.Type t = typeof(void);  
   }  
}  
```