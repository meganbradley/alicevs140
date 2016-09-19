---
title: "Compiler Error CS1010"
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
ms.assetid: 3d47277a-253f-464b-a603-e3b37e0e7b0d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1010
Newline in constant  
  
 A [string](../Topic/string%20\(C%23%20Reference\).md) was not properly delimited.  
  
 The following sample generates CS1010:  
  
```  
// CS1010.cs  
class Sample  
{  
   static void Main()  
   {  
      string a = "Hello World;   // CS1010  
      // Use the following line, with end quote before semicolon:  
      string a = "Hello World"; //  
   }  
}  
```  
  
## See Also  
 [NIB - Strings (C# Programming Guide)](assetId:///1a32b1c9-0d99-468a-9734-e3a47f2e897a)