---
title: "XML Value Property (Visual Basic)"
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
ms.assetid: 7ddd057a-a195-4e9b-ad8b-2ee0e615a20f
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML Value Property (Visual Basic)
Provides access to the value of the first element of a collection of <xref:System.Xml.Linq.XElement?qualifyHint=False> objects.  
  
## Syntax  
  
```  
  
object.Value  
```  
  
## Parts  
  
|||  
|-|-|  
|Term|Definition|  
|`object`|Required. Collection of <xref:System.Xml.Linq.XElement?qualifyHint=False> objects.|  
  
## Return Value  
 A `String` that contains the value of the first element of the collection, or `Nothing` if the collection is empty.  
  
## Remarks  
 The <xref:System.Xml.Linq.XElement.Value?qualifyHint=False> property makes it easy to access the value of the first element in a collection of <xref:System.Xml.Linq.XElement?qualifyHint=False> objects. This property first checks whether the collection contains at least one object. If the collection is empty, this property returns `Nothing`. Otherwise, this property returns the value of the <xref:System.Xml.Linq.XElement.Value?qualifyHint=False> property of the first element in the collection.  
  
> [!NOTE]
>  When you access the value of an XML attribute using the '@' identifier, the attribute value is returned as a `String` and you do not need to explicitly specify the <xref:System.Xml.Linq.XAttribute.Value?qualifyHint=False> property.  
  
 To access other elements in a collection, you can use the XML extension indexer property. For more information, see [XML Extension Indexer Property](../Topic/Extension%20Indexer%20Property%20\(Visual%20Basic\).md).  
  
## Inheritance  
 Most users will not have to implement <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False>, and can therefore ignore this section.  
  
 The <xref:System.Xml.Linq.XElement.Value?qualifyHint=False> property is an extension property for types that implement `IEnumerable(Of XElement)`. The binding of this extension property is like the binding of extension methods: if a type implements one of the interfaces and defines a property that has the name "Value", that property has precedence over the extension property. In other words, this <xref:System.Xml.Linq.XElement.Value?qualifyHint=False> property can be overridden by defining a new property in a class that implements `IEnumerable(Of XElement)`.  
  
## Example  
 The following example shows how to use the <xref:System.Xml.Linq.XElement.Value?qualifyHint=False> property to access the first node in a collection of <xref:System.Xml.Linq.XElement?qualifyHint=False> objects. The example uses the child axis property to get the collection of all child nodes named `phone` that are in the `contact` object.  
  
 [!CODE [VbXMLSamples#15](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#15)]  
  
 This code displays the following text:  
  
 `Phone number: 206-555-0144`  
  
## Example  
 The following example shows how to get the value of an XML attribute from a collection of <xref:System.Xml.Linq.XAttribute?qualifyHint=False> objects. The example uses the attribute axis property to display the value of the `type` attribute for all of the the `phone` elements.  
  
 [!CODE [VbXMLSamples#16](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#16)]  
  
 This code displays the following text:  
  
 `home`  
  
 `work`  
  
## See Also  
 <xref:System.Xml.Linq.XElement?qualifyHint=False>   
 <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False>   
 [XML Axis Properties](../Topic/XML%20Axis%20Properties%20\(Visual%20Basic\).md)   
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [Creating XML in Visual Basic](../vs140/Creating-XML-in-Visual-Basic.md)   
 [Extension Methods (Visual Basic)](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [XML Extension Indexer Property](../Topic/Extension%20Indexer%20Property%20\(Visual%20Basic\).md)   
 [XML Child Axis Property](../Topic/XML%20Child%20Axis%20Property%20\(Visual%20Basic\).md)   
 [XML Attribute Axis Property](../Topic/XML%20Attribute%20Axis%20Property%20\(Visual%20Basic\).md)