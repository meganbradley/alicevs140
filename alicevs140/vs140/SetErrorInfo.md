---
title: "SetErrorInfo"
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
ms.assetid: 78bca763-3f90-4e04-b566-b4b7fe2431b1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SetErrorInfo
Called by [OnWizFinish](../vs140/OnWizFinish.md) and [CanUseFileName](../vs140/CanUseFileName.md) to provide current error information.  
  
## Syntax  
  
```  
  
      function SetErrorInfo(   
   oErrorObj   
);  
```  
  
#### Parameters  
 *oErrorObj*  
 The error object.  
  
## Remarks  
 Called by [OnWizFinish](../vs140/OnWizFinish.md) and [CanUseFileName](../vs140/CanUseFileName.md) to provide current error information. See <xref:Microsoft.VisualStudio.VsWizard.VCWizCtlClass.SetErrorInfo?qualifyHint=False> in the Visual C++ Wizard Model documentation for more information.  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)