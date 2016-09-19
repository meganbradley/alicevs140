---
title: "Element names cannot use the &#39;xmlns&#39; prefix"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 88716bb5-6766-4180-b2ed-1d1bee0ff7a6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Element names cannot use the &#39;xmlns&#39; prefix
An XML element literal has been specified with an XML namespace prefix of `xmlns`. For example:  
  
```vb#  
Dim elem = <xmlns:ElementName>  
```  
  
 The XML 1.0 specification identifies `xmlns` as a reserved word.  
  
 **Error ID:** BC31189  
  
### To correct this error  
  
-   Change the XML namespace prefix to a valid value, or remove the prefix.  
  
## See Also  
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [Imports Statement (XML Namespace Prefix)](../vs140/Imports-Statement--XML-Namespace-.md)   
 [XML in Visual Basic](../Topic/XML%20in%20Visual%20Basic.md)