---
title: "CanAddClass"
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
ms.assetid: 76739742-1e34-470c-910d-8784f0adfbf0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CanAddClass
Called by the wizard to verify that the project is compatible with the code wizard the user is trying to run.  
  
## Syntax  
  
```  
  
      function CanAddClass(   
   oProj,   
   oObject    
);  
```  
  
#### Parameters  
 `oProj`  
 The selected project.  
  
 `oObject`  
 The selected object. In this case, the current project.  
  
## Return Value  
 **true** if the class can be added; otherwise **false**.  
  
## Remarks  
 The wizard calls this function when the parameter PREPROCESS_FUNCTION is in the [project control's .vsz file](../Topic/.Vsz%20File%20\(Project%20Control\).md).  
  
 It verifies if the [Visual C++ Code Model](assetId:///dd6452c2-1054-44a1-b0eb-639a94a1216b) object is available. If the code model is not available, the function reports an error and returns **false**.  
  
## Example  
  
```  
// Determine if a class can be added to the project  
if (CanAddClass(selProj, selObj))  
{  
   return true;  
}  
```  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)   
 [CanAddMFCClass](../vs140/CanAddMFCClass.md)   
 [CanAddATLClass](../vs140/CanAddATLClass.md)   
 [IsMFCProject](../vs140/IsMFCProject.md)