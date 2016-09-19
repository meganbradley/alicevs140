---
title: "LineBeginsWith"
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
ms.assetid: cbdd08ad-7309-4504-9f23-1c22bb3e4bd0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LineBeginsWith
Called by [InsertIntoFunction](../vs140/InsertIntoFunction.md) to determine if a line begins with the specified string.  
  
## Syntax  
  
```  
  
      function LineBeginsWith(   
   strBody,   
   strSearchString,   
   nStartPos    
);  
```  
  
#### Parameters  
 *strBody*  
 The body of the function.  
  
 `strSearchString`  
 The string to find.  
  
 *nStartPos*  
 The starting position for the search.  
  
## Return Value  
 **true** if the string is found; otherwise **false**.  
  
## Remarks  
 This function is called by `InsertIntoFunction` to determine if the specified line begins with the specified string.  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)   
 [OffsetToLineNumber](../vs140/OffsetToLineNumber.md)