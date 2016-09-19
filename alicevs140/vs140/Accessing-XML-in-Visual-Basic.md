---
title: "Accessing XML in Visual Basic"
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
ms.assetid: c47f88b2-3cbc-4bb1-b4b9-be60f71ffc6a
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Accessing XML in Visual Basic
[!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] provides XML axis properties for accessing and navigating [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] structures. These properties use a special syntax to enable you to access elements and attributes by specifying the XML names.  
  
 The following table lists the language features that enable you to access XML elements and attributes in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)].  
  
### XML Axis Properties  
  
|Property description|Example|Description|  
|--------------------------|-------------|-----------------|  
|*child axis*|`contact.<phone>`|Gets all `phone` elements that are child elements of the `contact` element.|  
|*attribute axis*|`phone.@type`|Gets all `type` attributes of the `phone` element.|  
|*descendant axis*|`contacts...<name>`|Gets all `name` elements of the `contacts` element, regardless of how deep in the hierarchy they occur.|  
|*extension indexer*|`contacts...<name>(0)`|Gets the first `name` element from the sequence.|  
|*value*|`contacts...<name>.Value`|Gets the string representation of the first object in the sequence, or `Nothing` if the sequence is empty.|  
  
## In This Section  
 [How to: Access XML Descendant Elements (Visual Basic)](../vs140/How-to--Access-XML-Descendant-Elements--Visual-Basic-.md)  
 Shows how to use a descendant axis property to access all XML elements that have a specified name and that are contained under a specified XML element.  
  
 [How to: Access XML Child Elements (Visual Basic)](../vs140/How-to--Access-XML-Child-Elements--Visual-Basic-.md)  
 Shows how to use a child axis property to access all XML child elements that have a specified name in an XML element.  
  
 [How to: Access XML Attributes (Visual Basic)](../vs140/How-to--Access-XML-Attributes--Visual-Basic-.md)  
 Shows how to use an attribute axis property to access all XML attributes that have a specified name in an XML element.  
  
 [How to: Declare and Use XML Namespace Prefixes](../vs140/How-to--Declare-and-Use-XML-Namespace-Prefixes--Visual-Basic-.md)  
 Shows how to declare an XML namespace prefix and use it to create and access XML elements.  
  
## Related Sections  
 [XML Axis Properties](../Topic/XML%20Axis%20Properties%20\(Visual%20Basic\).md)  
 Provides links to sections describing the various XML access properties.  
  
 [Overview of LINQ over XML in Visual Basic](../Topic/Overview%20of%20LINQ%20to%20XML%20in%20Visual%20Basic.md)  
 Provides an introduction to using [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] in Visual Basic.  
  
 [Creating XML in Visual Basic](../vs140/Creating-XML-in-Visual-Basic.md)  
 Provides an introduction to using XML literals in Visual Basic.  
  
 [Manipulating XML in Visual Basic](../Topic/Manipulating%20XML%20in%20Visual%20Basic.md)  
 Provides links to sections about loading and modifying XML in Visual Basic.  
  
 [XML in Visual Basic](../Topic/XML%20in%20Visual%20Basic.md)  
 Provides links to sections describing how to use [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] in Visual Basic.