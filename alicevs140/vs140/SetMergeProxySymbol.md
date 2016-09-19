---
title: "SetMergeProxySymbol"
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
ms.assetid: d6a9db59-2d5b-4431-98bc-785675e0eafe
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SetMergeProxySymbol
This function is called by the wizard to add the _MERGE_PROXYSTUB symbol if needed.  
  
## Syntax  
  
```  
  
      function SetMergeProxySymbol(   
   oProj    
);  
```  
  
#### Parameters  
 `oProj`  
 Selected project object  
  
## Remarks  
 This function is called by the wizard to add the _MERGE_PROXYSTUB symbol if needed.  
  
## Example  
  
```  
SetMergeProxySymbol (selproj);  
```  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)