---
title: "XML entity references are not supported"
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
ms.assetid: 2a393327-d8e2-4187-85b1-642b4f53b4ae
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML entity references are not supported
An entity reference (for example, `©`) that is not defined in the XML 1.0 specification is included as a value for an XML literal. Only `&`, `"`, `<`, `>`, and `'` XML entity references are supported in XML literals.  
  
 **Error ID:** BC31180  
  
### To correct this error  
  
-   Remove the unsupported entity reference.  
  
## See Also  
 [XML Literals and the XML 1.0 Specification](../vs140/XML-Literals-and-the-XML-1.0-Specification--Visual-Basic-.md)   
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [XML in Visual Basic](../Topic/XML%20in%20Visual%20Basic.md)