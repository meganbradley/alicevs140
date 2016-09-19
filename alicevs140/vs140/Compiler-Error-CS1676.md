---
title: "Compiler Error CS1676"
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
ms.assetid: 5ac83d98-5baa-49fd-b76a-d8ef0865b9dd
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1676
Parameter 'number' must be declared with the 'keyword' keyword  
  
 This error occurs when the parameter type modifier in an anonymous method is different from that used in the declaration of the delegate you are casting the method to.  
  
 The following sample generates CS1676:  
  
```  
// CS1676.cs  
delegate void E(ref int i);  
class Errors   
{  
   static void Main()  
   {  
      E e = delegate(out int i) { };   // CS1676  
      // To resolve, use the following line instead:  
      // E e = delegate(ref int i) { };  
   }  
}  
```