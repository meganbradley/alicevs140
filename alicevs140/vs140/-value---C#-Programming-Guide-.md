---
title: "&lt;value&gt; (C# Programming Guide)"
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
ms.assetid: 08dbadaf-9ab6-43d9-9493-98e43bed199a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;value&gt; (C# Programming Guide)
## Syntax  
  
```  
<value>property-description</value>  
```  
  
#### Parameters  
 `property-description`  
 A description for the property.  
  
## Remarks  
 The <value\> tag lets you describe the value that a property represents. Note that when you add a property via code wizard in the Visual Studio .NET development environment, it will add a [<summary\>](../vs140/-summary---C#-Programming-Guide-.md) tag for the new property. You should then manually add a <value\> tag to describe the value that the property represents.  
  
 Compile with [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md) to process documentation comments to a file.  
  
## Example  
 [!CODE [csProgGuideDocComments#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#14)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Recommended Tags for Documentation Comments](../vs140/Recommended-Tags-for-Documentation-Comments--C#-Programming-Guide-.md)