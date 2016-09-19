---
title: "&lt;seealso&gt; (C# Programming Guide)"
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
ms.assetid: 8e157f3f-f220-4fcf-9010-88905b080b18
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;seealso&gt; (C# Programming Guide)
## Syntax  
  
```  
<seealso cref="member"/>  
```  
  
#### Parameters  
 cref = " `member`"  
 A reference to a member or field that is available to be called from the current compilation environment. The compiler checks that the given code element exists and passes `member` to the element name in the output XML.`member` must appear within double quotation marks (" ").  
  
 For information on how to create a cref reference to a generic type, see [<see\> (C# Programmer's Reference)](../vs140/-see---C#-Programming-Guide-.md).  
  
## Remarks  
 The <seealso\> tag lets you specify the text that you might want to appear in a See Also section. Use [<see\>](../vs140/-see---C#-Programming-Guide-.md) to specify a link from within text.  
  
 Compile with [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md) to process documentation comments to a file.  
  
## Example  
 See [<summary\>](../vs140/-summary---C#-Programming-Guide-.md) for an example of using <seealso\>.  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Recommended Tags for Documentation Comments](../vs140/Recommended-Tags-for-Documentation-Comments--C#-Programming-Guide-.md)