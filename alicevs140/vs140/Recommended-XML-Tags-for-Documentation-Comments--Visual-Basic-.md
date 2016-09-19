---
title: "Recommended XML Tags for Documentation Comments (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 294e0736-ff1e-498e-af83-6db71ed41a72
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Recommended XML Tags for Documentation Comments (Visual Basic)
The [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler can process documentation comments in your code to an XML file. You can use additional tools to process the XML file into documentation.  
  
 XML comments are allowed on code constructs such as types and type members. For partial types, only one part of the type can have XML comments, although there is no restriction on commenting its members.  
  
> [!NOTE]
>  Documentation comments cannot be applied to namespaces. The reason is that one namespace can span several assemblies, and not all assemblies have to be loaded at the same time.  
  
 The compiler processes any tag that is valid XML. The following tags provide commonly used functionality in user documentation.  
  
||||  
|-|-|-|  
|[<c\>](../vs140/-c---Visual-Basic-.md)|[<code\>](../vs140/-code---Visual-Basic-.md)|[<example\>](../vs140/-example---Visual-Basic-.md)|  
|[<exception\>](../vs140/-exception---Visual-Basic-.md) <sup>1</sup>|[<include\>](../vs140/-include---Visual-Basic-.md) <sup>1</sup>|[<list\>](../vs140/-list---Visual-Basic-.md)|  
|[<para\>](../vs140/-para---Visual-Basic-.md)|[<param\>](../vs140/-param---Visual-Basic-.md) <sup>1</sup>|[<paramref\>](../vs140/-paramref---Visual-Basic-.md)|  
|[<permission\>](../Topic/%3Cpermission%3E%20\(Visual%20Basic\).md) <sup>1</sup>|[<remarks\>](../vs140/-remarks---Visual-Basic-.md)|[<returns\>](../vs140/-returns---Visual-Basic-.md)|  
|[<see\>](../vs140/-see---Visual-Basic-.md) <sup>1</sup>|[<seealso\>](../vs140/-seealso---Visual-Basic-.md) <sup>1</sup>|[<summary\>](../vs140/-summary---Visual-Basic-.md)|  
|[<typeparam\>](../vs140/-typeparam---Visual-Basic-.md) <sup>1</sup>|[<value\>](../vs140/-value---Visual-Basic-.md)||  
  
 (<sup>1</sup> The compiler verifies syntax.)  
  
> [!NOTE]
>  If you want angle brackets to appear in the text of a documentation comment, use `<` and `>`. For example, the string `"<text in angle brackets>"` will appear as `<text in angle``brackets>`.  
  
## See Also  
 [Documenting Your Code with XML (Visual Basic)](../vs140/Documenting-Your-Code-with-XML--Visual-Basic-.md)   
 [/doc](../vs140/-doc.md)   
 [How to: Create XML Documentation in Visual Basic](../vs140/How-to--Create-XML-Documentation-in-Visual-Basic.md)