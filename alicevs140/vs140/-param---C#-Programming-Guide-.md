---
title: "&lt;param&gt; (C# Programming Guide)"
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
ms.assetid: 46d329b1-5b84-4537-9e17-73ca97313e4e
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;param&gt; (C# Programming Guide)
## Syntax  
  
```  
<param name="name">description</param>  
```  
  
#### Parameters  
 `name`  
 The name of a method parameter. Enclose the name in double quotation marks (" ").  
  
 `description`  
 A description for the parameter.  
  
## Remarks  
 The <param\> tag should be used in the comment for a method declaration to describe one of the parameters for the method. To document multiple parameters, use multiple <param\> tags.  
  
 The text for the <param\> tag will be displayed in IntelliSense, the Object Browser, and in the Code Comment Web Report.  
  
 Compile with [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md) to process documentation comments to a file.  
  
## Example  
 [!CODE [csProgGuideDocComments#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#1)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Recommended Tags for Documentation Comments](../vs140/Recommended-Tags-for-Documentation-Comments--C#-Programming-Guide-.md)