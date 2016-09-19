---
title: "Finding the Default Paragraph Style (C#)"
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
ms.assetid: be102177-8ab0-444a-b671-7023e555ffdb
caps.latest.revision: 5
---
# Finding the Default Paragraph Style (C#)
The first task in the Manipulating Information in a WordprocessingML Document tutorial is to find the default style of paragraphs in the document.  
  
## Example  
  
### Description  
 The following example opens an Office Open XML WordprocessingML document, finds the document and style parts of the package, and then executes a query that finds the default style name. For information about Office Open XML document packages, and the parts they consist of, see [Details of Office Open XML WordprocessingML Documents (C#)](../vs140/Details-of-Office-Open-XML-WordprocessingML-Documents--C#-.md).  
  
 The query finds a node named `w:style` that has an attribute named `w:type` with a value of "paragraph", and also has an attribute named `w:default` with a value of "1". Because there will be only one XML node with these attributes, the query uses the <xref:System.Linq.Enumerable.First``1?qualifyHint=True> operator to convert a collection to a singleton. It then gets the value of the attribute with the name `w:styleId`.  
  
 This example uses classes from the WindowsBase assembly. It uses types in the <xref:System.IO.Packaging?qualifyHint=True> namespace.  
  
### Code  
  
```c#  
const string fileName = "SampleDoc.docx";  
  
const string documentRelationshipType =  
  "http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument";  
const string stylesRelationshipType =  
  "http://schemas.openxmlformats.org/officeDocument/2006/relationships/styles";  
const string wordmlNamespace =  
  "http://schemas.openxmlformats.org/wordprocessingml/2006/main";  
XNamespace w = wordmlNamespace;  
  
XDocument xDoc = null;  
XDocument styleDoc = null;  
  
using (Package wdPackage = Package.Open(fileName, FileMode.Open, FileAccess.Read))  
{  
    PackageRelationship docPackageRelationship =  
      wdPackage.GetRelationshipsByType(documentRelationshipType).FirstOrDefault();  
    if (docPackageRelationship != null)  
    {  
        Uri documentUri = PackUriHelper.ResolvePartUri(new Uri("/", UriKind.Relative),  
          docPackageRelationship.TargetUri);  
        PackagePart documentPart = wdPackage.GetPart(documentUri);  
  
        //  Load the document XML in the part into an XDocument instance.  
        xDoc = XDocument.Load(XmlReader.Create(documentPart.GetStream()));  
  
        //  Find the styles part. There will only be one.  
        PackageRelationship styleRelation =  
          documentPart.GetRelationshipsByType(stylesRelationshipType).FirstOrDefault();  
        if (styleRelation != null)  
        {  
            Uri styleUri = PackUriHelper.ResolvePartUri(documentUri, styleRelation.TargetUri);  
            PackagePart stylePart = wdPackage.GetPart(styleUri);  
  
            //  Load the style XML in the part into an XDocument instance.  
            styleDoc = XDocument.Load(XmlReader.Create(stylePart.GetStream()));  
        }  
    }  
}  
  
// The following query finds all the paragraphs that have the default style.  
string defaultStyle =   
    (string)(  
        from style in styleDoc.Root.Elements(w + "style")  
        where (string)style.Attribute(w + "type") == "paragraph"&&  
              (string)style.Attribute(w + "default") == "1"  
              select style  
    ).First().Attribute(w + "styleId");  
  
Console.WriteLine("The default style is: {0}", defaultStyle);  
```  
  
### Comments  
 This example produces the following output:  
  
```  
The default style is: Normal  
```  
  
## Next Steps  
 In the next example, you'll create a similar query that finds all the paragraphs in a document and their styles:  
  
-   [Retrieving the Paragraphs and Their Styles (C#)](../vs140/Retrieving-the-Paragraphs-and-Their-Styles--C#-.md)  
  
## See Also  
 [Manipulating Information in a WordprocessingML Document](../vs140/Tutorial--Manipulating-Content-in-a-WordprocessingML-Document.md)