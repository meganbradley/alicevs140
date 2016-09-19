---
title: "SetNoPchSettings"
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
ms.assetid: 52373c98-ad5e-4e9b-9e0f-9f58ddb2a636
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SetNoPchSettings
Sets up a project configuration properties when no precompiled header is used.  
  
## Syntax  
  
```  
  
      function SetNoPchSettings(   
   oProj    
);  
```  
  
#### Parameters  
 `oProj`  
 The selected project.  
  
## Remarks  
 Call this function to configure the project when the project uses no precompiled header settings.  
  
## Example  
 See [SetCommonPchSettings](../vs140/SetCommonPchSettings.md).  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)   
 [SetCommonPchSettings](../vs140/SetCommonPchSettings.md)   
 [AddCommonConfig](../Topic/AddCommonConfig.md)