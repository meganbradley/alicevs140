---
title: "&lt;see&gt; (C# Programming Guide)"
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
ms.assetid: 0200de01-7e2f-45c4-9094-829d61236383
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;see&gt; (C# Programming Guide)
## Syntax  
  
```  
<see cref="member"/>  
```  
  
#### Parameters  
 cref = " `member`"  
 A reference to a member or field that is available to be called from the current compilation environment. The compiler checks that the given code element exists and passes `member` to the element name in the output XML.Place *member* within double quotation marks (" ").  
  
## Remarks  
 The <see\> tag lets you specify a link from within text. Use [<seealso\>](../vs140/-seealso---C#-Programming-Guide-.md) to indicate that text should be placed in a See Also section. Use the [cref Attribute](../vs140/cref-Attribute--C#-Programming-Guide-.md) to create internal hyperlinks to documentation pages for code elements.  
  
 Compile with [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md) to process documentation comments to a file.  
  
 The following example shows a <see\> tag within a summary section.  
  
 [!CODE [csProgGuideDocComments#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#12)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Recommended Tags for Documentation Comments](../vs140/Recommended-Tags-for-Documentation-Comments--C#-Programming-Guide-.md)