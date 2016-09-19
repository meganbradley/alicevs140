---
title: "How to: Enable XML IntelliSense in Visual Basic"
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
ms.assetid: af67d0ee-a4a6-4abf-9c07-5a8cfe80d111
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Enable XML IntelliSense in Visual Basic
XML IntelliSense in Visual Basic provides word completion for elements that are defined in an XML schema. To enable XML IntelliSense in Visual Basic, you must do the following:  
  
1.  Obtain the XML schema (XSD) file or files for the XML files that your application will read from or write to.  
  
2.  Include the XML schema files in your project.  
  
3.  Import the target namespace or namespaces into your code file or project. A target namespace is identified by the `targetNamespace` or `tns` attribute of your XSD schema.  
  
     To import a target namespace, use the `Imports` statement, or add a namespace for all code files in a project by using the **References** page of the Project Designer.  
  
 For more information on the capabilities of XML IntelliSense in Visual Basic, see [XML Intellisense in Visual Basic](../Topic/XML%20IntelliSense%20in%20Visual%20Basic.md). For more information on importing XML namespaces, see [Imports Statement (XML Namespace Prefix)](../vs140/Imports-Statement--XML-Namespace-.md) or [References Page, Project Designer (Visual Basic)](../Topic/References%20Page,%20Project%20Designer%20\(Visual%20Basic\).md).  
  
 [!INCLUDE[note_settings_general](../vs140/includes/note_settings_general_md.md)]  
  
 ![link to video](../vs140/media/PlayVideo.gif "PlayVideo") For a video version of this topic, see [Video How to: Enable XML IntelliSense in Visual Basic](http://go.microsoft.com/fwlink/?LinkId=102466). For a related video demonstration, see [How Do I Enable XML IntelliSense and Use XML Namespaces?](http://go.microsoft.com/fwlink/?LinkId=143035).  
  
## Enable XML IntelliSense in Visual Basic  
 If you have an XML file but you do not have an XSD schema file for it, in SP1 you can create an XSD schema file by using the XML to Schema Wizard. You can also use schema inference in the Visual Studio XML Editor.  
  
#### To create an XSD schema file for an XML file by using the XML to Schema Wizard (requires SP1)  
  
1.  In your project, click **Add New Item** on the **Project** menu.  
  
2.  Select the **Xml to Schema** item template from either the **Data** or **Common Items** template categories.  
  
3.  Provide a file name for the XSD file or files that the inferred schema set will be stored in, and then click **Add**.  
  
4.  In the **Infer XML Schema set from XML documents** window, add one or more XML documents to infer the XML schema set from.  
  
    -   To add text files that contain XML documents by using File Explorer, click **Add from File**.  
  
    -   To add an XML document from an HTTP address, click **Add from Web**.  
  
    -   To copy or type the contents of an XML document into the wizard, click **Type or paste XML**.  
  
5.  When you have specified all the XML document sources from which you want to infer the XML schema set, click **OK** to infer the XML schema set. The schema set is saved in your project folder in one or more XSD files. (For each XML namespace in the schema, a file is created.)  
  
#### To create an XSD schema file for an XML file by using schema inference in the Visual Studio XML Editor  
  
1.  Edit the XML file in the Visual Studio XML Designer.  
  
2.  When the cursor is somewhere in the XML file, the **XML** menu appears. Click **Create Schema** on the **XML** menu. An XSD file is created from XSD schema inferred from the XML file.  
  
3.  Save the XSD schema file.  
  
    > [!NOTE]
    >  Different XSD schemas might be inferred from multiple XML documents that are intended to have the same schema. This can occur when particular elements and attributes are found in one XML file and not in another, or when elements are included in different order, for example. You should review inferred XSD schemas for completeness and accuracy when you use XSD schema inference.  
  
#### To include an XSD schema file  
  
-   By default, you cannot see XSD files in Visual Basic projects. If your XSD file is already included in the folders for your project, click the **Show All Files** button in **Solution Explorer**. Locate the XSD file in **Solution Explorer**, right-click the file, and click **Include File in Project**.  
  
-   If your XSD file is not already part of your project, in **Solution Explorer**, right-click the folder in which you want to store the XSD file, point to **Add**, and then click **Existing Item**. Locate your XSD file and then click **Add**.  
  
#### To import an XML namespace in a code file  
  
1.  Identify the target namespace from your XSD schema.  
  
2.  At the beginning of the code file, add an `Imports` statement for the target XML namespace, as shown in the following example.  
  
     [!CODE [VbXMLSamples#1](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#1)]  
  
     To import an XML namespace as the default namespace, that is, the namespace that is applied to XML elements and attributes that do not have a namespace prefix, add an `Imports` statement for the target default XML namespace. Do not specify a namespace prefix. Following is an example of an `Imports` statement.  
  
     [!CODE [VbXmlSamples#50](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#50)]  
  
#### To import an XML namespace for all files in a project  
  
1.  An XML namespace imported in a code file applies to that code file only. To import an XML namespace that applies to all code files in a project, open the Project Designer by double-clicking **My Project** in **Solution Explorer**.  
  
2.  On the **References** tab, in the **Imported namespaces** box, type the target XML namespace in the form of a full XML namespace declaration (for example, `<xmlns: ns="http://sampleNamespace">`). If the target XML namespace does not specify a namespace prefix, the namespace will be the default XML namespace for the project.  
  
3.  Click **Add User Import**.  
  
## See Also  
 [Imports Statement (XML Namespace Prefix)](../vs140/Imports-Statement--XML-Namespace-.md)   
 [References Page, Project Designer (Visual Basic)](../Topic/References%20Page,%20Project%20Designer%20\(Visual%20Basic\).md)   
 [XML Intellisense in Visual Basic](../Topic/XML%20IntelliSense%20in%20Visual%20Basic.md)