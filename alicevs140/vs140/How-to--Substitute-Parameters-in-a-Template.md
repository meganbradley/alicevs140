---
title: "How to: Substitute Parameters in a Template"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a62924a7-4ba0-413d-b606-fdbe1fcf2807
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Substitute Parameters in a Template
You may replace template parameters such as class names and namespaces when a file based on a template is created. For a complete list of template parameters, see [Parameter Substitution](../vs140/Template-Parameters.md).  
  
## Procedure  
 You may replace parameters in the files of a template whenever a project based on that template is created. This procedure explains how to create a template that replaces the name of a namespace with the safe project name when a new project is created with the template.  
  
#### To use a parameter to replace namespace name with the project name  
  
1.  Insert the parameter in one or more of the code files in the template. For example:  
  
    ```  
    namespace $safeprojectname$  
    ```  
  
    > [!NOTE]
    >  Template parameters are written in the format $*parameter*$.  
  
2.  In the .vstemplate file for the template, locate the `ProjectItem` element that includes this file.  
  
3.  Set the `ReplaceParameters` attribute to `true` for the `ProjectItem` element. For example:  
  
    ```  
    <ProjectItem ReplaceParameters="true">Class1.cs</ProjectItem>  
    ```  
  
## See Also  
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)   
 [Parameter Substitution](../vs140/Template-Parameters.md)   
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [ProjectItem Element (Visual Studio Template Content)](../vs140/ProjectItem-Element--Visual-Studio-Item-Templates-.md)