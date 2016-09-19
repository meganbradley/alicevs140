---
title: "Compiler Warning (level 4) CS0402"
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
ms.assetid: 5a252c95-18c7-4569-bae0-e1f7b582cf6a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) CS0402
'identifier' : an entry point cannot be generic or in a generic type  
  
 The entry point was found in a generic type. To remove this warning, implement Main in a non-generic class or struct.  
  
```  
// CS0402.cs  
// compile with: /W:4  
class C<T>  
{  
   public static void Main()  // CS0402  
   {  
  
   }  
}  
  
class CMain  
{  
   public static void Main() {}  
}  
```