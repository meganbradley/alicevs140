---
title: "Recommended Tags for Documentation Comments (Visual C++)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6548e798-5235-4a38-9482-bdc7b88f40a9
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Recommended Tags for Documentation Comments (Visual C++)
The Visual C++ compiler will process documentation comments in your code and creates an .xdc file for each compiland, and xdcmake.exe will process the .xdc files to an .xml file. Processing the .xml file to create documentation is a detail that needs to be implemented at your site.  
  
 Tags are processed on constructs such as types and type members.  
  
 Tags must immediately precede types or members.  
  
> [!NOTE]
>  Documentation comments cannot be applied to a namespace or on out of line definition for properties and events; documentation comments must on the in-class declarations.  
  
 The compiler will process any tag that is valid XML. The following tags provide commonly used functionality in user documentation:  
  
||||  
|-|-|-|  
|[<c\>](../vs140/-c---Visual-C---.md)|[<code\>](../vs140/-code---Visual-C---.md)|[<example\>](../vs140/-example---Visual-C---.md)|  
|[<exception\>](../vs140/-exception---Visual-C---.md)1|[<include\>](../vs140/-include---Visual-C---.md)1|[<list\>](../vs140/-list---Visual-C---.md)|  
|[<para\>](../vs140/-para---Visual-C---.md)|[<param\>](../vs140/-param---Visual-C---.md)1|[<paramref\>](../vs140/-paramref---Visual-C---.md)1|  
|[<permission\>](../Topic/%3Cpermission%3E%20\(Visual%20C++\).md)1|[<remarks\>](../vs140/-remarks---Visual-C---.md)|[<returns\>](../vs140/-returns---Visual-C---.md)|  
|[<see\>](../vs140/-see---Visual-C---.md)1|[<seealso\>](../vs140/-seealso---Visual-C---.md)1|[<summary\>](../vs140/-summary---Visual-C---.md)|  
|[<value\>](../vs140/-value---Visual-C---.md)|||  
  
 1. Compiler verifies syntax.  
  
 In the current release, the Visual C++ compiler does not support `<paramref>`, a tag that is supported by other Visual Studio compilers. Visual C++ may support `<paramref>` in a future release.  
  
## See Also  
 [XML Documentation](../vs140/XML-Documentation--Visual-C---.md)