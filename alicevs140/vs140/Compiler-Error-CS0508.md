---
title: "Compiler Error CS0508"
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
ms.assetid: 28403573-6e64-4496-918d-fb50c8851e51
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0508
'Type 1': return type must be 'Type 2' to match overridden member 'Member Name'  
  
 An attempt was made to change the return type in a method override. To resolve this error, make sure both methods declare the same return type.  
  
## Example  
 The following sample generates CS0508.  
  
```  
// CS0508.cs  
// compile with: /target:library  
abstract public class Clx  
{  
   public int i = 0;  
   // Return type is int.  
   abstract public int F();  
}  
  
public class Cly : Clx  
{  
   public override double F()  
   {  
      return 0.0;   // CS0508  
   }  
}  
```