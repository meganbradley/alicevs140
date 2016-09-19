---
title: "Attribute (XElement Dynamic Property)"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8440fc7d-b3b4-4726-8ec8-492e6af79642
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Attribute (XElement Dynamic Property)
Gets an indexer used to retrieve the attribute instance that corresponds to the specified expanded name.  
  
## Syntax  
  
```  
elem.Attribute[{namespaceName}attribName]  
```  
  
## Property Value/Return Value  
 An indexer of the type `XAttribute Item(String expandedName)`. This indexer takes the expanded name of the specified attribute and returns the corresponding <xref:System.Xml.Linq.XAttribute?qualifyHint=False>, or `null` if there is no attribute with the specified name.  
  
## Remarks  
 This property is equivalent to the <xref:System.Xml.Linq.XElement.Attribute?qualifyHint=False> method of the <xref:System.Xml.Linq.XElement?qualifyHint=True> class.  
  
## See Also  
 <xref:System.Xml.Linq.XElement.Attribute?qualifyHint=True>   
 [XElement Class Dynamic Properties](../Topic/XElement%20Class%20Dynamic%20Properties.md)   
 [Value (XAttribute Dynamic Property)](../vs140/Value--XAttribute-Dynamic-Property-.md)