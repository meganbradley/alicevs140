---
title: "Documenting Your Code with XML (Visual Basic)"
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
ms.assetid: a0d35dc7-c5f9-4d74-92ff-a1c6f28d5235
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Documenting Your Code with XML (Visual Basic)
In [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)], you can document your code using XML  
  
## XML Documentation Comments  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] provides an easy way to automatically create XML documentation for projects. You can automatically generate an XML skeleton for your types and members, and then provide summaries, descriptive documentation for each parameter, and other remarks. With the appropriate setup, the XML documentation is automatically emitted into an XML file with the same name as your project and the .xml extension. For more information, see [/doc](../vs140/-doc.md).  
  
 The XML file can be consumed or otherwise manipulated as XML. This file is located in the same directory as the output .exe or .dll file of your project.  
  
 XML documentation starts with `'''`. The processing of these comments has some restrictions:  
  
-   The documentation must be well-formed XML. If the XML is not well formed, a warning is generated and the documentation file contains a comment saying that an error was encountered.  
  
-   Developers are free to create their own set of tags. There is a recommended set of tags (see "Related Sections" in this topic). Some of the recommended tags have special meanings:  
  
    -   The <param\> tag is used to describe parameters. If used, the compiler will verify that the parameter exists and that all parameters are described in the documentation. If the verification fails, the compiler issues a warning.  
  
    -   The `cref` attribute can be attached to any tag to provide a reference to a code element. The compiler verifies that this code element exists. If the verification fails, the compiler issues a warning. The compiler also respects any `Imports` statements when looking for a type described in the `cref` attribute.  
  
    -   The <summary\> tag is used by IntelliSense in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] to display additional information about a type or member.  
  
## Related Sections  
 For details on creating an XML file with documentation comments, see the following topics:  
  
-   [/doc](../vs140/-doc.md)  
  
-   [Recommended XML Tags for Documentation Comments (Visual Basic)](../vs140/Recommended-XML-Tags-for-Documentation-Comments--Visual-Basic-.md)  
  
-   [Processing the XML File (Visual Basic)](../vs140/Processing-the-XML-File--Visual-Basic-.md)  
  
-   [How to: Create XML Documentation in Visual Basic](../vs140/How-to--Create-XML-Documentation-in-Visual-Basic.md)  
  
-   [XML in Visual Studio](../vs140/XML-Tools-in-Visual-Studio.md)  
  
## See Also  
 [Developing Applications with Visual Basic](../vs140/Developing-Applications-with-Visual-Basic.md)   
 [Visual Basic Language Guide](../vs140/Visual-Basic-Programming-Guide.md)