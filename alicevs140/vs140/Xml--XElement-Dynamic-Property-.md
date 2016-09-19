---
title: "Xml (XElement Dynamic Property)"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - XElement.Xml
ms.assetid: 69ab2a33-4fe7-4cfa-97f8-eaf063decb18
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Xml (XElement Dynamic Property)
Gets the unformatted XML content of the element.  
  
## Syntax  
  
```  
elem.Xml  
```  
  
## Property Value/Return Value  
 A <xref:System.String?qualifyHint=False> that represents the unformatted XML content of the element.  
  
## Remarks  
 This property is equivalent to the <xref:System.Xml.Linq.XNode.ToString(System.Xml.Linq.SaveOptions)?qualifyHint=False> method of the <xref:System.Xml.Linq.XNode?qualifyHint=True> class, with the `SaveOptions` parameter set to <xref:System.Xml.Linq.SaveOptions.DisableFormatting?qualifyHint=False>.  
  
## See Also  
 [XElement Class Dynamic Properties](../Topic/XElement%20Class%20Dynamic%20Properties.md)   
 [Value (XElement Dynamic Property)](../Topic/Value%20\(XElement%20Dynamic%20Property\).md)