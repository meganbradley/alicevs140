---
title: "&lt;paramref&gt; (C# Programming Guide)"
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
ms.assetid: 756c24c1-f591-40e8-a838-559761539b0b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;paramref&gt; (C# Programming Guide)
## Syntax  
  
```  
<paramref name="name"/>  
```  
  
#### Parameters  
 `name`  
 The name of the parameter to refer to. Enclose the name in double quotation marks (" ").  
  
## Remarks  
 The <paramref\> tag gives you a way to indicate that a word in the code comments, for example in a <summary\> or <remarks\> block refers to a parameter. The XML file can be processed to format this word in some distinct way, such as with a bold or italic font.  
  
 Compile with [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md) to process documentation comments to a file.  
  
## Example  
 [!CODE [csProgGuideDocComments#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#7)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Recommended Tags for Documentation Comments](../vs140/Recommended-Tags-for-Documentation-Comments--C#-Programming-Guide-.md)