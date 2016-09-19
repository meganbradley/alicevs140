---
title: "IsMFCProject"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 98dd57df-9fdb-40d7-afcf-4b99e9d54dad
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IsMFCProject
Checks if a project is MFC based.  
  
## Syntax  
  
```  
  
      function IsMFCProject(   
   oProj,   
   bCWinAppRequired    
);  
```  
  
#### Parameters  
 `oProj`  
 The selected project  
  
 *bCWinAppRequired*  
 Indicates whether extension DLLs are included in the check.  
  
## Return Value  
 **true** if the project is an MFC project; otherwise **false**.  
  
## Remarks  
 Use this function to determine if the selected project is an MFC project.  
  
## Example  
  
```  
if (!IsMFCProject(selProj, true))  
   {  
      if (gbExceptionThrown)  
         return false;  
      var L_ErrMsg2_Text = "ATL support can only be added to MFC EXEs or MFC Regular DLLs.";  
      wizard.ReportError(L_ErrMsg2_Text);  
      return false;  
   }  
```  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)   
 [IsATLProject](../vs140/IsATLProject.md)   
 [IsAttributedProject](../vs140/IsAttributedProject.md)