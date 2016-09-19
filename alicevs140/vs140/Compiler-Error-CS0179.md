---
title: "Compiler Error CS0179"
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
ms.assetid: bef000ca-64d7-4809-b2a0-de6927b04b0d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0179
'member' cannot be extern and declare a body  
  
 When a class member is marked [extern](../Topic/extern%20\(C%23%20Reference\).md), it means that the member's definition is located in another file. Therefore, a class member marked as **extern** cannot be defined in the class. Either remove the `extern` keyword or delete the definition. For more information, see [Class and Struct Methods (C# Programmer's Reference)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0179:  
  
```  
// CS0179.cs  
public class MyClass  
{  
   public extern int ExternMethod(int aa)   // CS0179  
   {  
      return 0;  
   }  
   // try the following line instead  
   // public extern int ExternMethod(int aa);  
  
   public static void Main()  
   {  
   }  
}  
```