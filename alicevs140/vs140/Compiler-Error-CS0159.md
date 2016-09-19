---
title: "Compiler Error CS0159"
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
ms.assetid: 9fde7ffa-aed7-4a9d-8f47-ea67bc9df9e4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0159
No such label 'label' within the scope of the goto statement  
  
 The label referenced by the [goto](../vs140/goto--C#-Reference-.md) statement could not be found within the scope of the `goto` statement.  
  
 The following sample generates CS0159:  
  
```  
// CS0159.cs  
public class Class1  
{  
   public static void Main()  
   {  
      int i = 0;  
  
      switch (i)  
      {  
         case 1:  
            goto case 3;   // CS0159, case 3 label does not exist  
         case 2:  
            break;  
      }  
      goto NOWHERE;   // CS0159, NOWHERE label does not exist  
   }  
}  
```