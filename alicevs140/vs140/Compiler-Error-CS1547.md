---
title: "Compiler Error CS1547"
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
ms.assetid: 40029557-076a-47d8-aabc-d86c56a846d7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1547
Keyword 'void' cannot be used in this context  
  
 The compiler detected an invalid use of the [void](../vs140/void--C#-Reference-.md) keyword.  
  
 The following sample generates CS1547:  
  
```  
// CS1547.cs  
public class MyClass  
{  
   void BadMethod()  
   {  
      void i;   // CS1547, cannot have variables of type void  
   }  
  
   public static void Main()  
   {  
   }  
}  
```