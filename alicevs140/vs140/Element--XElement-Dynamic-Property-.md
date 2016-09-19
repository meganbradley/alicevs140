---
title: "Element (XElement Dynamic Property)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - XElement.Element
apitype: Assembly
ms.assetid: c6c25b8d-a1da-41ff-aeff-867ff1dcf749
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Element (XElement Dynamic Property)
Gets an indexer used to retrieve the child element instance that corresponds to the specified expanded name.  
  
## Syntax  
  
```  
elem.Element[{namespaceName}localName]  
```  
  
## Property Value/Return Value  
 An indexer of the type `XElement Item(String expandedName)`. This indexer takes an expanded name parameter and returns the corresponding <xref:System.Xml.Linq.XElement?qualifyHint=False>, or `null` if there is no element with the specified name.  
  
## Remarks  
 This property is equivalent to <xref:System.Xml.Linq.XContainer.Element?qualifyHint=False> method of the <xref:System.Xml.Linq.XContainer?qualifyHint=True> class.  
  
## See Also  
 <xref:System.Xml.Linq.XContainer.Element?qualifyHint=True>   
 [XElement Class Dynamic Properties](../Topic/XElement%20Class%20Dynamic%20Properties.md)   
 [Elements (XElement Dynamic Property)](../vs140/Elements--XElement-Dynamic-Property-.md)