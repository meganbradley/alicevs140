---
title: "GetProjectFile"
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
ms.assetid: e5fdc468-755a-4b4e-81bd-e63881531bed
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetProjectFile
Returns the file name specified type.  
  
## Syntax  
  
```  
  
      function GetProjectFile(   
   oProj,   
   strType,   
   bFullPath,   
   bMFC    
);  
```  
  
#### Parameters  
 oProj  
 The selected project.  
  
 `strType`  
 The type of file to retrieve, such as STDAFX, RC, IDL, CPP, H, ODL, or DEF.  
  
 *bFullPath*  
 Flag indicating whether to return the full path name.  
  
 *bMFC*  
 Indicates if the project is an MFC-based project. If `strType` is .cpp or .h, it is considered MFC based. If not, the project is assumed to be ATL based.  
  
## Return Value  
 The file name of the per-project type of files.  
  
## Remarks  
 Call this function to get the file name of the specified type in the specified project.  
  
## Example  
  
```  
// The selected MFC project's CPP file is retrieved and   
// assigned to strFileName.  
var strFileName = GetProjectFile(selProj, "CPP", false, true);  
```  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)   
 [GetProjectPath](../vs140/GetProjectPath.md)   
 [GetUniqueFileName](../vs140/GetUniqueFileName.md)