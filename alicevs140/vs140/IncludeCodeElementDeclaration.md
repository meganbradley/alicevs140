---
title: "IncludeCodeElementDeclaration"
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
ms.assetid: 714e76e4-76bc-439a-982a-cf9d4ada7677
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IncludeCodeElementDeclaration
Adds the include statement to `strInFile`, including the header where `strCodeElemName` is implemented, if such a header found in the `oProj`.  
  
## Syntax  
  
```  
  
      function IncludeCodeElementDeclaration(   
   oProj,   
   strCodeElemName,   
   strInFile    
);  
```  
  
#### Parameters  
 `oProj`  
 The selected project.  
  
 `strCodeElemName`  
 The full name of the code element for which you are searching the definition header.  
  
 `strInFile`  
 The file that will include the definition header, if found.  
  
## Remarks  
 Adds the include statement to `strInFile`, including the header where `strCodeElemName` is implemented, if such a header found in `oProj`.  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)