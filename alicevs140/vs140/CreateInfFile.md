---
title: "CreateInfFile"
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
ms.assetid: 941ea2ce-db10-428e-b423-8dc2a7e825cf
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CreateInfFile
Creates the wizard's Templates.inf file.  
  
## Syntax  
  
```  
  
function CreateInfFile( );  
  
```  
  
## Return Value  
 The wizard template file.  
  
## Remarks  
 Call this function to create the wizard's Templates.inf file from Templatesinf.txt, a temporary text file it first creates in the temporary directory, based on the user's selections. Templates.inf contains the list of file names that the wizard creates. See [The Template File](../vs140/Template-Files.md) for more information.  
  
 If this function cannot create the Templatesinf.txt file in the temporary directory, it displays an error.  
  
## Example  
 See [AddFilesToProject](../vs140/AddFilesToProject.md).  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)   
 [AddFilesToProject](../vs140/AddFilesToProject.md)   
 [SetFilters](../vs140/SetFilters.md)   
 [AddFilesToProject](../vs140/AddFilesToProject.md)