---
title: "XML literals and XML properties are not supported in embedded code within ASP.NET"
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
ms.assetid: 053e8cba-8584-45cc-9fa0-43d122779772
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML literals and XML properties are not supported in embedded code within ASP.NET
XML literals and XML properties are not supported in embedded code within ASP.NET. To use XML features, move the code to code-behind.  
  
 An XML literal or XML axis property is defined within embedded code (`<%= =>`) in an ASP.NET file.  
  
 **Error ID:** BC31200  
  
### To correct this error  
  
-   Move the code that includes the XML literal or XML axis property to an ASP.NET code-behind file.  
  
## See Also  
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [XML Axis Properties](../Topic/XML%20Axis%20Properties%20\(Visual%20Basic\).md)   
 [XML in Visual Basic](../Topic/XML%20in%20Visual%20Basic.md)