---
title: "XML literals and XML axis properties are not available"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cb861748-0ee4-40d3-a859-98ca6c39b4f4
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML literals and XML axis properties are not available
XML literals and XML axis properties are not available. Add references to System.Xml, System.Xml.Linq, and System.Core.  
  
 The code being compiled includes XML literals or XML axis properties, but it does not reference the assemblies that are needed to compile XML literals or XML axis properties.  
  
 **Error ID:** BC31190  
  
### To correct this error  
  
-   Add references to the System.Xml.dll, System.Xml.Linq.dll, and System.Core.dll assemblies.  
  
## See Also  
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [XML Axis Properties](../Topic/XML%20Axis%20Properties%20\(Visual%20Basic\).md)   
 [XML in Visual Basic](../Topic/XML%20in%20Visual%20Basic.md)