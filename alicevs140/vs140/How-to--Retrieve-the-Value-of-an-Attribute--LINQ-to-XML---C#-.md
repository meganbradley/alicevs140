---
title: "How to: Retrieve the Value of an Attribute (LINQ to XML) (C#)"
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
ms.assetid: 817bbe89-5979-4234-bf0c-46f63692ac8c
caps.latest.revision: 5
---
# How to: Retrieve the Value of an Attribute (LINQ to XML) (C#)
This topic shows how to obtain the value of attributes. There are two main ways: You can cast an <xref:System.Xml.Linq.XAttribute?qualifyHint=False> to the desired type; the explicit conversion operator then converts the contents of the element or attribute to the specified type. Alternatively, you can use the <xref:System.Xml.Linq.XAttribute.Value?qualifyHint=False> property. However, casting is generally the better approach. If you cast the attribute to a nullable type, the code is simpler to write when retrieving the value of an attribute that might or might not exist. For examples of this technique, see [How to: Retrieve the Value of an Element (LINQ to XML) (C#)](../vs140/How-to--Retrieve-the-Value-of-an-Element--LINQ-to-XML---C#-.md).  
  
## Example  
 To retrieve the value of an attribute, you just cast the <xref:System.Xml.Linq.XAttribute?qualifyHint=False> object to your desired type.  
  
```c#  
XElement root = new XElement("Root",  
                    new XAttribute("Attr", "abcde")  
                );  
Console.WriteLine(root);  
string str = (string)root.Attribute("Attr");  
Console.WriteLine(str);  
```  
  
 This example produces the following output:  
  
```  
<Root Attr="abcde" />  
abcde  
```  
  
## Example  
 The following example shows how to retrieve the value of an attribute where the attribute is in a namespace. For more information, see [Working with XML Namespaces (C#)](../Topic/Working%20with%20XML%20Namespaces%20\(C%23\).md).  
  
```c#  
XNamespace aw = "http://www.adventure-works.com";  
XElement root = new XElement(aw + "Root",  
                    new XAttribute(aw + "Attr", "abcde")  
                );  
string str = (string)root.Attribute(aw + "Attr");  
Console.WriteLine(str);  
```  
  
 This example produces the following output:  
  
```  
abcde  
```  
  
## See Also  
 [LINQ to XML Axes (C#)](../vs140/LINQ-to-XML-Axes--C#-.md)