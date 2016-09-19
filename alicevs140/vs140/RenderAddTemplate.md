---
title: "RenderAddTemplate"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 84c898d6-8676-4ae1-9245-c023e1c9ab92
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RenderAddTemplate
Renders a template file and optionally adds it to the project.  
  
## Syntax  
  
```  
  
      function RenderAddTemplate(   
   strTemplateFile,   
   strProjectFile,   
   ProjToAddTo,   
   bOpen    
);  
```  
  
#### Parameters  
 *strTemplateFile*  
 The template file name only, excluding path, relative to TEMPLATES_PATH.  
  
 *strProjectFile*  
 The name of new file created. This string may include the path, but relative to PROJECT_PATH.  
  
 *ProjToAddTo*  
 The project object. Provide the project name if the created file must be added to the project; otherwise, disregard or pass **false** if you are not adding the file to the project.  
  
 *bOpen*  
 If **true**, open the file in the default editor after adding it to the project.  
  
## Remarks  
 Call this function to render a template file and optionally adds it to the project.  
  
## Example  
  
```  
// Declare the project path and the template path.  
var strProjectPath = wizard.FindSymbol("PROJECT_PATH");  
var strTemplatePath = wizard.FindSymbol("TEMPLATES_PATH");  
// Declare the template header and implementation files.  
var strTemplateHeader = wizard.FindSymbol("TEMPLATE_HEADER");  
var strTemplateImpl = wizard.FindSymbol("TEMPLATE_IMPL");  
// Render the template strTemplateHeader and open it in the editor.  
RenderAddTemplate(strTemplateHeader, strHeaderFile, selProj, true);   
// Render the template strTemplateImpl, but do not open it   
// in the editor.  
RenderAddTemplate(strTemplateImpl, strImplFile, selProj, false);  
```  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)