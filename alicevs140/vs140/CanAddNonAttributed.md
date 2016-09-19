---
title: "CanAddNonAttributed"
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
ms.assetid: a2b0143e-f84b-40f3-8f51-23a492f651f8
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CanAddNonAttributed
Indicates that the ATL project supports nonattributed objects.  
  
## Syntax  
  
```  
  
function CanAddNonAttributed( );  
  
```  
  
## Return Value  
 **true** if the project supports nonattributed and attributed ATL objects; **false** if the project supports only attributed projects.  
  
## Remarks  
 Call this function to indicate whether the project supports both nonattributed and attributed objects.  
  
## Example  
  
```  
// Check if attributed project using CanAddNonAttributed  
window.external.Load(document);  
if (IsAttributedProject(window.external))  
{  
   ATTRIBUTED.checked = true;  
   if (!CanAddNonAttributed())  
      ATTRIBUTED.disabled = true;  
}  
```  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)   
 [Concepts](../vs140/Attributed-Programming-Concepts.md)   
 [CanAddClass](../vs140/CanAddClass.md)