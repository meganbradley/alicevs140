---
title: "&lt;typeparam&gt; (C# Programming Guide)"
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
ms.assetid: 9b99d400-e911-4e55-99c6-64367c96aa4f
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;typeparam&gt; (C# Programming Guide)
## Syntax  
  
```  
<typeparam name="name">description</typeparam>  
```  
  
#### Parameters  
 `name`  
 The name of the type parameter. Enclose the name in double quotation marks (" ").  
  
 `description`  
 A description for the type parameter.  
  
## Remarks  
 The `<typeparam>` tag should be used in the comment for a generic type or method declaration to describe a type parameter. Add a tag for each type parameter of the generic type or method.  
  
 For more information, see [Generics (C# Programmer's Reference)](../Topic/Generics%20\(C%23%20Programming%20Guide\).md).  
  
 The text for the `<typeparam>` tag will be displayed in IntelliSense, the [Object Browser Window](assetId:///3c7f1673-1f0d-41b1-94ca-a3dcfcb82cda) code comment web report.  
  
 Compile with [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md) to process documentation comments to a file.  
  
## Example  
 [!CODE [csProgGuideDocComments#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#13)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Recommended Tags for Documentation Comments (C# Programmer's Reference)](../vs140/Recommended-Tags-for-Documentation-Comments--C#-Programming-Guide-.md)