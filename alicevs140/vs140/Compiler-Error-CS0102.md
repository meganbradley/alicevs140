---
title: "Compiler Error CS0102"
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
ms.assetid: c9419779-649f-4c24-b0f3-f0a1be46659e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0102
The type 'type name' already contains a definition for 'identifier'  
  
 A class contains multiple declarations for identifiers with the same name at the same scope. To fix the error, rename the duplicate identifiers.  
  
## Example  
 The following sample generates CS0102.  
  
```  
// CS0102.cs  
// compile with: /target:library  
namespace MyApp  
{  
   public class MyClass  
   {  
      string s = "Hello";  
      string s = "Goodbye";   // CS0102  
  
      public void GetString()  
      {  
         string s = "Hello again";   // method scope, no error  
      }  
   }  
}  
  
```