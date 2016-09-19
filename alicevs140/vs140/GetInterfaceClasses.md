---
title: "GetInterfaceClasses"
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
ms.assetid: 712c112f-b4ff-43c4-ad49-c4f4c13c48bd
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetInterfaceClasses
Returns the `VCCodeClass` object associated with an interface.  
  
## Syntax  
  
```  
  
      function GetInterfaceClasses(   
   strInterface,   
   oProject,   
   aryClasses    
);  
```  
  
#### Parameters  
 *strInterface*  
 The name of the interface containing the class objects.  
  
 *oProject*  
 The selected project.  
  
 *aryClasses*  
 [out] An array of class objects in the interface.  
  
## Return Value  
 The <xref:Microsoft.VisualStudio.VCCodeModel.VCCodeClass?qualifyHint=False> object associated with an interface.  
  
## Remarks  
 Call this function to retrieve the classes associated with an interface.  
  
## Example  
  
```  
var aryClasses = new Array();  
GetInterfaceClasses(oInterface.Name, selProj, aryClasses);  
```  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)   
 [GetInterfaceType](../vs140/GetInterfaceType.md)