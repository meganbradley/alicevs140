---
title: "Namespace declaration with prefix cannot have an empty value in XML literals"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dde656b4-df3b-4a2e-8871-4e14832ca778
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Namespace declaration with prefix cannot have an empty value in XML literals
An XML namespace declaration in an XML literal does not include a namespace value. For example, the following code will cause this error:  
  
```vb#  
Dim book = <book xmlns:ns=""/>  
```  
  
 **Error ID:** BC31184  
  
### To correct this error  
  
-   Include a valid namespace in the XML namespace declaration, or remove the XML namespace declaration from the XML literal.  
  
     As an alternative, you can use the `Imports` statement to identify a namespace prefix for the empty namespace. For example:  
  
    ```vb#  
    Imports <xmlns:ns="">  
    ```  
  
## See Also  
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [XML in Visual Basic](../Topic/XML%20in%20Visual%20Basic.md)   
 [Imports Statement (XML Namespace)](../vs140/Imports-Statement--XML-Namespace-.md)