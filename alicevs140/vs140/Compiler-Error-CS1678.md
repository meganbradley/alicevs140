---
title: "Compiler Error CS1678"
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
ms.assetid: 2be8aa17-81e2-47b0-b239-e41e0c5c0d97
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1678
Parameter 'number' is declared as type 'type1' but should be 'type2'  
  
 This error occurs when the parameter type in an anonymous method is different from the declaration of the delegate you are casting the method to.  
  
 The following sample generates CS1678:  
  
```  
// CS1678  
delegate void D(int i);  
class Errors   
{  
   static void Main()   
   {  
      D d = delegate(string s) { };   // CS1678  
      // To resolve, use the following line instead:  
      // D d = delegate(int s) { };  
   }  
}  
```