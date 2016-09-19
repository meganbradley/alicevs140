---
title: "LINQ to XML Annotations3"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: LINQ to XML Annotations
ms.assetid: 54e7b9d0-07f5-488f-9065-b6e6b870f810
caps.latest.revision: 5
---
# LINQ to XML Annotations3
Annotations in [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] enable you to associate any arbitrary object of any arbitrary type with any XML component in an XML tree.  
  
 To add an annotation to an XML component, such as an <xref:System.Xml.Linq.XElement?qualifyHint=False> or <xref:System.Xml.Linq.XAttribute?qualifyHint=False>, you call the <xref:System.Xml.Linq.XObject.AddAnnotation?qualifyHint=False> method. You retrieve annotations by type.  
  
 Note that annotations are not part of the XML infoset; they are not serialized or deserialized.  
  
## Methods  
 You can use the following methods when working with annotations:  
  
|Method|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XObject.AddAnnotation?qualifyHint=False>|Adds an object to the annotation list of an <xref:System.Xml.Linq.XObject?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XObject.Annotation?qualifyHint=False>|Gets the first annotation object of the specified type from an <xref:System.Xml.Linq.XObject?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XObject.Annotations?qualifyHint=False>|Gets a collection of annotations of the specified type for an <xref:System.Xml.Linq.XObject?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XObject.RemoveAnnotations?qualifyHint=False>|Removes the annotations of the specified type from an <xref:System.Xml.Linq.XObject?qualifyHint=False>.|  
  
## See Also  
 [Advanced LINQ to XML Programming (C#)](../Topic/Advanced%20LINQ%20to%20XML%20Programming%20\(C%23\).md)