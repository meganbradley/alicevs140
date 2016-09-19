---
title: "Errors occurred while compiling the XML schemas in the project"
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
ms.assetid: 9323b5d2-ba14-4e49-91f1-9ad647162144
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Errors occurred while compiling the XML schemas in the project
Errors occurred while compiling the XML schemas in the project. Because of this, XML IntelliSense is not available.  
  
 There is an error in an XML Schema Definition (XSD) schema included in the project. This error occurs when you add an XSD schema (.xsd) file that conflicts with the existing XSD schema set for the project.  
  
 **Error ID:** BC36810  
  
### To correct this error  
  
-   Double-click the warning in the **Errors List** window. Visual Basic will take you to the location in the XSD file that is the source of the warning. Correct the error in the XSD schema.  
  
-   Ensure that all required XSD schema (.xsd) files are included in the project. You may need to click **Show All Files** on the **Project** menu to see your .xsd files in **Solution Explorer**. Right-click an .xsd file and then click **Include In Project** to include the file in your project.  
  
-   If you are using the XML to Schema Wizard, this error can occur if you infer schemas more than one time from the same source. In this case, you can remove the existing XSD schema files from the project, add a new XML to Schema item template, and then provide the XML to Schema Wizard with all the applicable XML sources for your project.  
  
-   If no error is identified in your XSD schema, the XML compiler may not have enough information to provide a detailed error message. You may be able to get more detailed error information if you ensure that the XML namespaces for the .xsd files included in your project match the XML namespaces identified for the XML Schema set in Visual Studio.  
  
## See Also  
 [Error List Window](../vs140/Error-List-Window.md)   
 [XML Intellisense in Visual Basic](../Topic/XML%20IntelliSense%20in%20Visual%20Basic.md)   
 [XML in Visual Basic](../Topic/XML%20in%20Visual%20Basic.md)