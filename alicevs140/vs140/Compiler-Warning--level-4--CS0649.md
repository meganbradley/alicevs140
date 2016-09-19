---
title: "Compiler Warning (level 4) CS0649"
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
ms.assetid: 37137b18-12ed-4a0f-92e6-ee5fb0532ef3
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) CS0649
Field 'field' is never assigned to, and will always have its default value 'value'  
  
 The compiler detected an uninitialized private or internal field declaration that is never assigned a value.  
  
 The following sample generates CS0649:  
  
```  
// CS0649.cs  
// compile with: /W:4  
using System.Collections;  
  
class MyClass  
{  
   Hashtable table;  // CS0649  
   // You may have intended to initialize the variable to null  
   // Hashtable table = null;  
  
   // Or you may have meant to create an object here  
   // Hashtable table = new Hashtable();  
  
   public void Func(object o, string p)  
   {  
      // Or here  
      // table = new Hashtable();  
      table[p] = o;  
   }  
  
   public static void Main()  
   {  
   }  
}  
```