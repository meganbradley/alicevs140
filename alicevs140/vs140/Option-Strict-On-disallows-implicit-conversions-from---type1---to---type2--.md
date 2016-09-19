---
title: "Option Strict On disallows implicit conversions from &#39;&lt;type1&gt;&#39; to &#39;&lt;type2&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b9756d48-05fa-4027-8a80-b4a0ef92099d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option Strict On disallows implicit conversions from &#39;&lt;type1&gt;&#39; to &#39;&lt;type2&gt;&#39;
You have tried to convert a type to another type that may not be able to contain the value, such as a `Long` to an `Integer`, while the type checking switch ([Option Strict Statement](../vs140/Option-Strict-Statement.md)) is set to `On`.  
  
 This type of conversion is called a *narrowing conversion*, and it is possible for it to fail at run time. For this reason, `Option Strict On` disallows implicit narrowing conversions.  
  
 **Error ID:** BC30512  
  
### To correct this error  
  
1.  Determine whether a conversion of any type exists from `<type1>` to `<type2>`. If both are [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] elementary types, or if both are instances of classes, you can usually make this determination by consulting the table in [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md).  
  
2.  If only a narrowing conversion exists from `<type1>` to `<type2>`, you should use explicit casting. The [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md) and [DirectCast](../Topic/DirectCast%20Operator%20\(Visual%20Basic\).md) keywords throw a run-time exception if the conversion fails. The [TryCast](../Topic/TryCast%20Operator%20\(Visual%20Basic\).md) keyword applies only to reference types and returns [Nothing (Visual Basic)](../Topic/Nothing%20\(Visual%20Basic\).md) if the conversion fails.  
  
3.  If a narrowing conversion exists and your program can tolerate a run-time failure, or you are confident that a run-time failure is not possible, you can specify `Option Strict Off` at the beginning of your source code. But you should still enclose the conversion in a [Try...Catch...Finally Statement (Visual Basic)](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md) block to avoid unexpected results or early termination of your program.  
  
4.  If no conversion exists from `<type1>` to `<type2>`, you must re-evaluate your program logic. You might be able to write code that can assign values to `<type2>` corresponding to anticipated values of `<type1>`.  
  
5.  If no conversion exists from `<type1>` to `<type2>` and one of the types is a class or structure you have defined, you might be able to define a conversion operator from that type to or from the other type. For more information, see [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md).  
  
6.  In all cases and as a general guideline, you should avoid using narrowing conversions unless you can trap failures in a `Catch` block and deal with them effectively.  
  
## See Also  
 [Option Strict Statement](../vs140/Option-Strict-Statement.md)   
 [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)   
 [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md)   
 [DirectCast](../Topic/DirectCast%20Operator%20\(Visual%20Basic\).md)   
 [TryCast](../Topic/TryCast%20Operator%20\(Visual%20Basic\).md)   
 [Nothing (Visual Basic)](../Topic/Nothing%20\(Visual%20Basic\).md)   
 [Try...Catch...Finally Statement (Visual Basic)](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)