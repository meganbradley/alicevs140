---
title: "How to: Catch Parsing Errors (C#)"
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
ms.assetid: bfb612d4-5605-48ef-8c93-915cf9d5dcfb
caps.latest.revision: 5
---
# How to: Catch Parsing Errors (C#)
This topic shows how to detect badly formed or invalid XML.  
  
 [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] is implemented using <xref:System.Xml.XmlReader?qualifyHint=False>. If badly formed or invalid XML is passed to [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)], the underlying <xref:System.Xml.XmlReader?qualifyHint=False> class will throw an exception. The various methods that parse XML, such as <xref:System.Xml.Linq.XElement.Parse?qualifyHint=True>, do not catch the exception; the exception can then be caught by your application.  
  
## Example  
 The following code tries to parse invalid XML:  
  
```c#  
try {  
    XElement contacts = XElement.Parse(  
        @"<Contacts>  
            <Contact>  
                <Name>Jim Wilson</Name>  
            </Contact>  
          </Contcts>");  
  
    Console.WriteLine(contacts);  
}  
catch (System.Xml.XmlException e)  
{  
    Console.WriteLine(e.Message);  
}  
```  
  
 When you run this code, it throws the following exception:  
  
```  
The 'Contacts' start tag on line 1 does not match the end tag of 'Contcts'. Line 5, position 13.  
```  
  
 For information about the exceptions that you can expect the <xref:System.Xml.Linq.XElement.Parse?qualifyHint=True>, <xref:System.Xml.Linq.XDocument.Parse?qualifyHint=True>, <xref:System.Xml.Linq.XElement.Load?qualifyHint=True>, and <xref:System.Xml.Linq.XDocument.Load?qualifyHint=True> methods to throw, see the <xref:System.Xml.XmlReader?qualifyHint=False> documentation.  
  
## See Also  
 [Parsing XML (C#)](../vs140/Parsing-XML--C#-.md)