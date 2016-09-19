---
title: "OffsetToLineNumber"
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
ms.assetid: ac7e3c22-6b3b-432c-85cc-b50bbef9ce8c
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OffsetToLineNumber
Called by [InsertIntoFunction](../vs140/InsertIntoFunction.md) to convert an index in a function body to a line number.  
  
## Syntax  
  
```  
  
      function OffsetToLineNumber(   
   strString,   
   nPos    
);  
```  
  
#### Parameters  
 `strString`  
 The string containing the function body. The function body is a multi-line string where its lines are delimited by cr-lf character pairs.  
  
 `nPos`  
 A position within the string.  
  
## Return Value  
 The line within the body function where `nPos` is located. The first line in the function is considered to be line 1 (not 0).  
  
## Remarks  
 Finds the line number for a given position in a function body.  
  
 This function is called by `InsertIntoFunction` to convert the index located at `nPos` in a function body to a line number.  
  
## Example  
  
```  
strString = "function DelFile(fso,  
 strWizTempFile)\r\n{\r\n\ttry\r\n\t{\r\nif   
(fso.FileExists(strWizTempFile))\r\nreturn true;\r\n";  
  
nLine =  OffsetToLineNumber(strString, 60);  
  
// The return value for the above is 5, because character 60 in the string   
// occurs in the 5th line within the string.  
```  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)   
 [LineBeginsWith](../vs140/LineBeginsWith.md)