---
title: "Expression cannot appear inside a quoted attribute value"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ed3e618e-de94-4e4e-afaf-72b11073fb1d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expression cannot appear inside a quoted attribute value
Expression cannot appear inside a quoted attribute value. Try removing quotes.  
  
 An embedded expression in an attribute value for an XML literal is contained within quotation marks.  
  
 **Error ID:** BC31155  
  
### To correct this error  
  
-   Remove the delimiting quotation marks from the attribute value. The following is an example:  
  
    ```vb#  
    ' Generates an error.  
    Dim elem = <outer attr="<%= value %>" />  
  
    ' Does not generate an error.  
    Dim elem = <outer attr=<%= value %> />  
    ```  
  
## See Also  
 [Embedded Expressions In XML](../Topic/Embedded%20Expressions%20in%20XML%20\(Visual%20Basic\).md)   
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [XML in Visual Basic](../Topic/XML%20in%20Visual%20Basic.md)