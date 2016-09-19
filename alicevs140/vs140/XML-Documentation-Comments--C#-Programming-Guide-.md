---
title: "XML Documentation Comments (C# Programming Guide)"
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
ms.assetid: 803b7f7b-7428-4725-b5db-9a6cff273199
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML Documentation Comments (C# Programming Guide)
In Visual C# you can create documentation for your code by including XML elements in special comment fields (indicated by triple slashes) in the source code directly before the code block to which the comments refer, for example:  
  
```  
/// <summary>  
///  This class performs an important function.  
/// </summary>  
public class MyClass{}  
```  
  
 When you compile with the [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md) option, the compiler will search for all XML tags in the source code and create an XML documentation file. To create the final documentation based on the compiler-generated file, you can create a custom tool or use a tool such as [Sandcastle](http://go.microsoft.com/fwlink/?LinkId=124061).  
  
 To refer to XML elements (for example, your function processes specific XML elements that you want to describe in an XML documentation comment), you can use the standard quoting mechanism (`<` and `>`).  To refer to generic identifiers in code reference (`cref`) elements, you can use either the escape characters (for example, `cref=”List<T>”`) or braces (`cref=”List{T}”`).  As a special case, the compiler parses the braces as angle brackets to make the documentation comment less cumbersome to author when referring to generic identifiers.  
  
> [!NOTE]
>  The XML documentation comments are not metadata; they are not included in the compiled assembly and therefore they are not accessible through reflection.  
  
## In This Section  
  
-   [Recommended Tags for Documentation Comments](../vs140/Recommended-Tags-for-Documentation-Comments--C#-Programming-Guide-.md)  
  
-   [Processing the XML File](../vs140/Processing-the-XML-File--C#-Programming-Guide-.md)  
  
-   [Delimiters for Documentation Tags](../vs140/Delimiters-for-Documentation-Tags--C#-Programming-Guide-.md)  
  
-   [How to: Use the XML Documentation Features](../vs140/How-to--Use-the-XML-Documentation-Features--C#-Programming-Guide-.md)  
  
## Related Sections  
 For more information, see:  
  
-   [/doc (Process Documentation Comments)](../Topic/-doc%20\(C%23%20Compiler%20Options\).md)  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)