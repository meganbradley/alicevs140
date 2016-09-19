---
title: "Templates.inf File"
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
ms.assetid: 93d60d27-2402-4dc8-a829-e97417ccea49
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Templates.inf File
Templates.inf is a text file that contains a list of templates to render for the project.  
  
 Because Templates.inf is a [template file](../vs140/Template-Files.md) itself, you can use directives to indicate which files to include in a project, depending on a user's selections. See [Template Directives](../vs140/Template-Directives.md) for a list of directives that you can use in this file.  
  
## Example  
  
```  
Template1.txt  
Template2.txt  
  [!if TYPE_A]  
TemplateOptionA.h  
TemplateOptionA.cpp  
  [!else]  
TemplateOptionB.h  
TemplateOptionB.cpp  
  [!endif]  
```  
  
 **CreateCustomInfFile** renders Templates.inf into a temporary text file, which must then be deleted after processing the files.  
  
## Example  
  
```  
var InfFile = CreateCustomInfFile();  
AddFilesToProject(selProj, strProjectName, InfFile);  
InfFile.Delete();  
```  
  
 See [The JScript File](../vs140/JScript-File.md) for more information.  
  
## See Also  
 [Files Created for Your Wizard](../vs140/Files-Created-for-Your-Wizard.md)   
 [Custom Wizard](../vs140/Custom-Wizard.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)