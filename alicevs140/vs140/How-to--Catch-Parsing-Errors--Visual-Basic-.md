---
title: "How to: Catch Parsing Errors (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 22e9068e-ea58-447b-816e-cd1852c11787
caps.latest.revision: 3
---
# How to: Catch Parsing Errors (Visual Basic)
This topic shows how to detect badly formed or invalid XML.  
  
 [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] is implemented using <xref:System.Xml.XmlReader?qualifyHint=False>. If badly formed or invalid XML is passed to [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)], the underlying <xref:System.Xml.XmlReader?qualifyHint=False> class will throw an exception. The various methods that parse XML, such as <xref:System.Xml.Linq.XElement.Parse?qualifyHint=True>, do not catch the exception; the exception can then be caught by your application.  
  
 Note that you cannot get parse errors if you use XML literals. The Visual Basic compiler will catch errors of badly formed or invalid XML.  
  
## Example  
 The following code tries to parse invalid XML:  
  
```vb  
Try  
    Dim contacts As XElement = XElement.Parse("<Contacts>" & vbCrLf & _  
        "    <Contact>" & vbCrLf & _  
        "        <Name>Jim Wilson</Name>" & vbCrLf & _  
        "    </Contact>" & vbCrLf & _  
        "</Contcts>")  
  
    Console.WriteLine(contacts)  
Catch e As System.Xml.XmlException  
    Console.WriteLine(e.Message)  
End Try  
```  
  
 When you run this code, it throws the following exception:  
  
```  
The 'Contacts' start tag on line 1 does not match the end tag of 'Contcts'. Line 5, position 13.  
```  
  
 For information about the exceptions that you can expect the <xref:System.Xml.Linq.XElement.Parse?qualifyHint=True>, <xref:System.Xml.Linq.XDocument.Parse?qualifyHint=True>, <xref:System.Xml.Linq.XElement.Load?qualifyHint=True>, and <xref:System.Xml.Linq.XDocument.Load?qualifyHint=True> methods to throw, see the <xref:System.Xml.XmlReader?qualifyHint=False> documentation.  
  
## See Also  
 [Parsing XML (Visual Basic)](../Topic/Parsing%20XML%20\(Visual%20Basic\).md)