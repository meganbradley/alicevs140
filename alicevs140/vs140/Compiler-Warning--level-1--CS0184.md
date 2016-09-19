---
title: "Compiler Warning (level 1) CS0184"
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
ms.assetid: 55e73f76-f502-4d15-88fc-bd5757b512a4
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS0184
The given expression is never of the provided ('type') type  
  
 The expression can never be **true** because the variable you are testing is neither declared as ***type*** nor derived from ***type***.  
  
 The following sample generates CS0184:  
  
```  
// CS0184.cs  
// compile with: /W:1  
class MyClass  
{  
   public static void Main()  
   {  
      int i = 0;  
      if (i is string)   // CS0184  
         i++;  
   }  
}  
```