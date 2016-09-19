---
title: "Compiler Warning (level 2) CS0464"
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
ms.assetid: 3dff97d4-e1f6-4a71-91e2-68cffc38d49a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS0464
Comparing with null of type 'type' always produces 'false'  
  
 This warning is produced when you perform a comparison between a nullable variable and null, and the comparison is not `==` or `!=`. To resolve this error, verify if you really want to check a value for `null`. A comparison like `i == null` can be either true of false. A comparison like `i > null` is always false.  
  
## Example  
 The following sample generates CS0464.  
  
```  
// CS0464.cs  
class MyClass  
{  
   public static void Main()  
   {  
      int? i = 0;  
      if (i < null) ;   // CS0464  
  
      i++;  
   }  
}  
```