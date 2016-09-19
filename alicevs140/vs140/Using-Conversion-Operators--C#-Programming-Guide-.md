---
title: "Using Conversion Operators (C# Programming Guide)"
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
ms.assetid: caf36e89-c6c0-4b87-9f9e-85780a45c9a4
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using Conversion Operators (C# Programming Guide)
You can use `implicit` conversion operators, which are easier to use, or `explicit` conversion operators, which clearly indicate to anyone reading the code that you're converting a type. This topic demonstrates both types of conversion operator.  
  
> [!NOTE]
>  For information about simple type conversions, see [How to: Convert a String to a Number (C# Programming Guide)](../Topic/How%20to:%20Convert%20a%20String%20to%20a%20Number%20\(C%23%20Programming%20Guide\).md), [How to: Convert a byte Array to an int (C# Programming Guide)](../Topic/How%20to:%20Convert%20a%20byte%20Array%20to%20an%20int%20\(C%23%20Programming%20Guide\).md), [How to: Convert Between Hexadecimal Strings and Numeric Types (C# Programming Guide)](../Topic/How%20to:%20Convert%20Between%20Hexadecimal%20Strings%20and%20Numeric%20Types%20\(C%23%20Programming%20Guide\).md), or <xref:System.Convert?qualifyHint=False>.  
  
## Example  
 This is an example of an explicit conversion operator. This operator converts from the type <xref:System.Byte?qualifyHint=False> to a value type called `Digit`. Because not all bytes can be converted to a digit, the conversion is explicit, meaning that a cast must be used, as shown in the `Main` method.  
  
 [!CODE [csProgGuideStatements#11](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#11)]  
  
## Example  
 This example demonstrates an implicit conversion operator by defining a conversion operator that undoes what the previous example did: it converts from a value class called `Digit` to the integral <xref:System.Byte?qualifyHint=False> type. Because any digit can be converted to a <xref:System.Byte?qualifyHint=False>, there's no need to force users to be explicit about the conversion.  
  
 [!CODE [csProgGuideStatements#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#12)]  
  
## See Also  
 [C# Programmer's Reference](../vs140/C#-Reference.md)   
 [C# Programming](../vs140/C#-Programming-Guide.md)   
 [Conversion Operators (C#)](../Topic/Conversion%20Operators%20\(C%23%20Programming%20Guide\).md)   
 [is (C# Reference)](../vs140/is--C#-Reference-.md)