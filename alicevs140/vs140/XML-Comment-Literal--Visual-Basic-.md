---
title: "XML Comment Literal (Visual Basic)"
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
ms.assetid: 634c1cee-5e01-48d0-88d7-2dd55e4a9e52
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML Comment Literal (Visual Basic)
A literal representing an <xref:System.Xml.Linq.XComment?qualifyHint=False> object.  
  
## Syntax  
  
```  
<!-- content -->  
```  
  
## Parts  
  
|||  
|-|-|  
|Term|Definition|  
|`<!--`|Required. Denotes the start of the XML comment.|  
|`content`|Required. Text to appear in the XML comment. Cannot contain a series of two hyphens (--) or end with a hyphen adjacent to the closing tag.|  
|`-->`|Required. Denotes the end of the XML comment.|  
  
## Return Value  
 An <xref:System.Xml.Linq.XComment?qualifyHint=False> object.  
  
## Remarks  
 XML comment literals do not contain document content; they contain information about the document. The XML comment section ends with the sequence "-->". This implies the following points:  
  
-   You cannot use an embedded expression in an XML comment literal because the embedded expression delimiters are valid XML comment content.  
  
-   XML comment sections cannot be nested, because `content` cannot contain the value "-->".  
  
 You can assign an XML comment literal to a variable, or you can include it in an XML element literal.  
  
> [!NOTE]
>  An XML literal can span multiple lines without using line continuation characters. This feature enables you to copy content from an XML document and paste it directly into a [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] program.  
  
 The [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler converts the XML comment literal to a call to the <xref:System.Xml.Linq.XComment.#ctor?qualifyHint=False> constructor.  
  
## Example  
 The following example creates an XML comment that contains the text "This is a comment".  
  
 [!CODE [VbXMLSamples#9](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#9)]  
  
## See Also  
 <xref:System.Xml.Linq.XComment?qualifyHint=False>   
 [XML Element Literal](../Topic/XML%20Element%20Literal%20\(Visual%20Basic\).md)   
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [Creating XML in Visual Basic](../vs140/Creating-XML-in-Visual-Basic.md)