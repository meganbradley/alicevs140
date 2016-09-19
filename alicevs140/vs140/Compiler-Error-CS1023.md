---
title: "Compiler Error CS1023"
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
ms.assetid: 27d70f2c-9ae1-459c-a6be-01ed5a3eea07
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1023
Embedded statement cannot be a declaration or labeled statement  
  
 An embedded statement, such as the statements following an **if** statement, can contain neither declarations nor labeled statements.  
  
 The following sample generates CS1023 twice:  
  
```  
// CS1023.cs  
public class a  
{  
   public static void Main()  
   {  
      if (1)  
         int i;      // CS1023, declaration is not valid here  
  
      if (1)  
         xx : i++;   // CS1023, labeled statement is not valid here  
   }  
}  
```