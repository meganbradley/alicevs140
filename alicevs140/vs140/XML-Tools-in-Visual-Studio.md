---
title: "XML Tools in Visual Studio"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1fd5de47-2d61-4180-9539-c2c4bf9ab768
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML Tools in Visual Studio
*Extensible Markup Language (XML)* is a markup language that provides a format for describing data. This facilitates more precise declarations of content and more meaningful search results across multiple platforms. In addition, XML enables the separation of presentation from data. For example, in HTML you use tags to tell the browser to display data as bold or italic; in XML you use tags only to describe data, such as city name, temperature, and barometric pressure. In XML you use style sheets such as Extensible Stylesheet Language (XSL) and cascading style sheets (CSS) to present the data in a browser. XML separates the data from the presentation and the process. This enables you to display and process the data as you want to, by applying different style sheets and applications.  
  
 XML is a subset of SGML that is optimized for delivery over the Web. It is defined by the World Wide Web Consortium (W3C). This standardization guarantees that structured data will be uniform and independent of applications or vendors.  
  
 XML is at the core of many features of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] and the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)]. The following topic list names the tools and features related to XML that are offered in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] and the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)].  
  
 For more information, see the [XML Developer Center](http://go.microsoft.com/fwlink/?LinkID=100176), which provides the latest documentation, technical information, downloads, newsgroups, and other resources for XML developers.  
  
## In This Section  
 [Working with XML Data](../vs140/Working-with-XML-Data.md)  
 Discusses the role of XML in the way data is handled in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 [Debugging XSLT](../vs140/Debugging-XSLT.md)  
 Provides links to topics about using the Visual Studio debugger to debug XSLT.  
  
## Reference  
 [Microsoft.VisualStudio.XmlEditor](http://go.microsoft.com/fwlink/?LinkID=165699)  
 Exposes the [XML Editor](http://go.microsoft.com/fwlink/?LinkId=228249) parse tree through [System.Xml.Linq](http://go.microsoft.com/fwlink/?LinkId=228250) for any XML documents.  
  
 [XML Standards Reference](assetId:///79c78508-c9d0-423a-a00f-672e855de401)  
 Provides information about XML technologies, including XML, Document Type Definition (DTD), XML Schema definition language (XSD), and XSLT.  
  
 <xref:System.Xml?qualifyHint=True>  
 Describes the classes and other elements that make up the <xref:System.Xml?qualifyHint=False> namespace and provides links to more detailed information on each item.  
  
 <xref:System.Xml.Serialization?qualifyHint=True>  
 Describes the classes and other elements that make up the <xref:System.Xml.Serialization?qualifyHint=False> namespace and provides links to more detailed information about each item.  
  
## Related Sections  
 [XML Document Object Model (DOM)](assetId:///b5e52844-4820-47c0-a61d-de2da33e9f54)  
 Describes how the <xref:System.Xml.XmlDocument?qualifyHint=False> and its associated classes comply with the W3C Document Object Model (Core) Level 1 and Level 2 namespace support specifications.  
  
 [Reading XML with the XmlReader](assetId:///3029834c-a27e-4331-b7aa-711924062182)  
 Describes how the <xref:System.Xml.XmlReader?qualifyHint=False> provides noncached, forward only, read-only access to XML data over an XML stream.  
  
 [Writing XML with the XmlWriter](assetId:///ea41f72c-e1d3-4e0a-ab0f-f0eb1c27ab86)  
 Describes how the <xref:System.Xml.XmlWriter?qualifyHint=False> provides noncached, forward only, way of generating XML streams and helps you build XML documents that comply with the W3C standard.  
  
 [XSLT Transformations](assetId:///202f8820-224c-494f-b61e-cd127eac6e03)  
 Describes how the <xref:System.Xml.Xsl.XslCompiledTransform?qualifyHint=False> class implements the XSLT 1.0 recommendation.  
  
 [Process XML Data Using the XPath Data Model](assetId:///536c6fce-1453-4654-9c72-bca54d47e081)  
 Describes how the <xref:System.Xml.XPath.XPathNavigator?qualifyHint=False> class can process XML data stored in an <xref:System.Xml.XPath.XPathDocument?qualifyHint=False> or an <xref:System.Xml.XmlDocument?qualifyHint=False> object. The <xref:System.Xml.XPath.XPathNavigator?qualifyHint=False> class is based on the XQuery 1.0 and XPath 2.0 Data Model and can be used to navigate and edit XML data.  
  
 [XML Schema Object Model (SOM)](assetId:///a897a599-ffd1-43f9-8807-e58c8a7194cd)  
 Describes the classes used for creating and manipulating XML Schemas, by providing an <xref:System.Xml.Schema.XmlSchema?qualifyHint=False> class to load and edit a schema.