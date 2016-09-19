---
title: "sizeof (C# Reference)"
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
ms.assetid: c548592c-677c-4f40-a4ce-e613f7529141
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sizeof (C# Reference)
Used to obtain the size in bytes for an unmanaged type. Unmanaged types include the built-in types that are listed in the table that follows, and also the following:  
  
-   Enum types  
  
-   Pointer types  
  
-   User-defined structs that do not contain any fields or properties that are reference types  
  
 The following example shows how to retrieve the size of an `int`:  
  
```c#  
// Constant value 4:  
int intSize = sizeof(int);   
```  
  
## Remarks  
 Starting with version 2.0 of C#, applying `sizeof` to built-in types no longer requires that [unsafe](../vs140/unsafe--C#-Reference-.md) mode be used.  
  
 The `sizeof` operator cannot be overloaded. The values returned by the `sizeof` operator are of type `int`. The following table shows the constant values that are substituted for `sizeof` expressions that have certain built-in types as operands.  
  
|Expression|Constant value|  
|----------------|--------------------|  
|`sizeof(sbyte)`|1|  
|`sizeof(byte)`|1|  
|`sizeof(short)`|2|  
|`sizeof(ushort)`|2|  
|`sizeof(int)`|4|  
|`sizeof(uint)`|4|  
|`sizeof(long)`|8|  
|`sizeof(ulong)`|8|  
|`sizeof(char)`|2 (Unicode)|  
|`sizeof(float)`|4|  
|`sizeof(double)`|8|  
|`sizeof(decimal)`|16|  
|`sizeof(bool)`|1|  
  
 For all other types, including structs, the `sizeof` operator can be used only in unsafe code blocks. Although you can use the <xref:System.Runtime.InteropServices.Marshal.SizeOf?qualifyHint=True> method, the value returned by this method is not always the same as the value returned by `sizeof`. <xref:System.Runtime.InteropServices.Marshal.SizeOf?qualifyHint=True> returns the size after the type has been marshaled, whereas `sizeof` returns the size as it has been allocated by the common language runtime, including any padding.  
  
## Example  
 [!CODE [csrefKeywordsOperator#11](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#11)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Operator Keywords](../vs140/Operator-Keywords--C#-Reference-.md)   
 [enum](../Topic/enum%20\(C%23%20Reference\).md)   
 [Unsafe Code and Pointers (C# Programming Guide)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md)   
 [Structs (C# Programming Guide)](../vs140/Structs--C#-Programming-Guide-.md)   
 [Constants (C# Programming Guide)](../Topic/Constants%20\(C%23%20Programming%20Guide\).md)