---
title: "&lt;permission&gt; (C# Programming Guide)"
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
ms.assetid: 769e93fe-8404-443f-bf99-577aa42b6a49
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;permission&gt; (C# Programming Guide)
## Syntax  
  
```  
<permission cref="member">description</permission>  
```  
  
#### Parameters  
 cref = " `member`"  
 A reference to a member or field that is available to be called from the current compilation environment. The compiler checks that the given code element exists and translates `member` to the canonical element name in the output XML. *member* must appear within double quotation marks (" ").  
  
 For information on how to create a cref reference to a generic type, see [<see\> (C# Programmer's Reference)](../vs140/-see---C#-Programming-Guide-.md).  
  
 `description`  
 A description of the access to the member.  
  
## Remarks  
 The <permission\> tag lets you document the access of a member. The <xref:System.Security.PermissionSet?qualifyHint=False> class lets you specify access to a member.  
  
 Compile with [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md) to process documentation comments to a file.  
  
## Example  
 [!CODE [csProgGuideDocComments#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#8)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Recommended Tags for Documentation Comments](../vs140/Recommended-Tags-for-Documentation-Comments--C#-Programming-Guide-.md)