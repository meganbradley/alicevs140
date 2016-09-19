---
title: "Compiler Error CS1609"
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
ms.assetid: 89e112f8-6337-4803-8741-2e38497deb8c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1609
Modifiers cannot be placed on event accessor declarations  
  
 Modifiers can only be placed on event declarations and not on the event accessor declarations. For more information, see [Using Properties (C# Programming Guide)](../vs140/Using-Properties--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS1609.  
  
```  
// CS1609.cs  
// compile with: /target:library  
delegate int Del();  
class A  
{  
   public event Del MyEvent   
   {  
      private add {}   // CS1609  
      // try the following line instead  
      // add {}  
      remove {}  
   }  
}  
```