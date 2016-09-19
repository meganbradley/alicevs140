---
title: "Compiler Error CS1029"
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
ms.topic: error-reference
ms.assetid: 61bd4d44-9bfc-42bb-a9f0-a0683da53640
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1029
\#error: 'text'  
  
 Displays the text of an error defined with the [#error](../vs140/#error--C#-Reference-.md) directive.  
  
 The following sample shows how to create a user-defined error:  
  
```  
// CS1029.cs  
class Sample  
{  
   static void Main()  
   {  
      #error Let's give an error here   // CS1029  
   }  
}  
```