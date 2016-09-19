---
title: "Compiler Error CS0037"
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
ms.assetid: 1d34a71e-10a0-4fa8-9b94-343e69428c61
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0037
Cannot convert null to 'type' because it is a non-nullable value type  
  
 The compiler cannot assign null to a value type; null can only be assigned to a [reference type](../vs140/Reference-Types--C#-Reference-.md) or to a Nullable type. [struct](../vs140/struct--C#-Reference-.md) is a value type. For more information, see [Nullable Types (C# Programmers Reference)](../Topic/Nullable%20Types%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0037:  
  
```  
// CS0037.cs  
public struct s  
{  
}  
  
class a  
{  
   public static void Main()  
   {  
      int i = null;   // CS0037  
      s ss = null;    // CS0037  
   }  
}  
```