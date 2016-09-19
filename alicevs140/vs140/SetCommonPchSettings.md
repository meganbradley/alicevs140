---
title: "SetCommonPchSettings"
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
ms.assetid: 12f5524b-f654-4222-b979-8ee0d9f58c14
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SetCommonPchSettings
Establishes the precompiled header settings for the project.  
  
## Syntax  
  
```  
  
      function SetCommonPchSettings(   
   oProj    
);  
```  
  
#### Parameters  
 `oProj`  
 The selected project.  
  
## Remarks  
 Call this function to establish the precompiled header settings for the project.  
  
 This function sets the <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.UsePrecompiledHeader?qualifyHint=False> property to the following:  
  
-   **pchUseUsingSpecific** Uses the [/Yu (Use Precompiled Header File)](../vs140/-Yu--Use-Precompiled-Header-File-.md) compiler setting.  
  
-   **pchCreateUsingSpecific** Uses the [/Yc (Create Precompiled Header File)](../vs140/-Yc--Create-Precompiled-Header-File-.md) compiler setting.  
  
## Example  
  
```  
if ((strAppType == "LIB" || ((strAppType == "CONSOLE") &&   
   wizard.FindSymbol(SUPPORT_MFC"))) && !Pch)  
   {  
      AddFilesToProject(selProj, strProjectName, InfFile);  
      SetNoCommonPchSettings(selProj);  
   }  
else  
   {  
      AddFilesToProject(selProj, strProjectName, InfFile);  
      SetcommonPchSettings(selProj);  
   }  
```  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)   
 [SetNoPchSettings](../vs140/SetNoPchSettings.md)   
 [AddCommonConfig](../Topic/AddCommonConfig.md)