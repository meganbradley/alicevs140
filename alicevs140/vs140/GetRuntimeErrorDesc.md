---
title: "GetRuntimeErrorDesc"
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
ms.assetid: d56fdd2e-6ad0-4c49-9e98-bcf0105e1b12
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetRuntimeErrorDesc
Returns a description for the exception type.  
  
## Syntax  
  
```  
  
      function GetRuntimeErrorDesc(   
   strRuntimeErrorName    
);  
```  
  
#### Parameters  
 *strRuntimeErrorName*  
 The name of the type of exception that has occurred.  
  
## Return Value  
 A description of the exception type.  
  
## Remarks  
 Returns a description for the exception type. Can be one of the following exception types:  
  
|Exception types|Description|  
|---------------------|-----------------|  
|ConversionError|Occurs whenever there is an attempt to convert an object into something to which it cannot be converted.|  
|RangeError|Occurs when a function is supplied with an argument that has exceeded its allowable range. For example, this error occurs if you attempt to construct an `Array` object with a length that is not a valid positive integer.|  
|ReferenceError|Occurs when an invalid reference has been detected. This error will occur, for example, if an expected reference is null.|  
|RegExpError|Occurs when a compilation error occurs with a regular expression. Once the regular expression is compiled, this error cannot occur. This example will occur, for example, when a regular expression is declared with a pattern that has an invalid syntax, or flags other than *i*, *g*, or *m*, or if it contains the same flag more than once.|  
|SyntaxError|Occurs when source text is parsed and that source text does not follow correct syntax. This error will occur, for example, if the `eval` function is called with an argument that is not valid program text.|  
|TypeError|Occurs whenever the actual type of an operand does not match the expected type. An example of when this error occurs is a function call made on something that is not an object or does not support the call.|  
|URIError|Occurs when an illegal Uniform Resource Indicator (URI) is detected. For example, this is error occurs when an illegal character is found in a string being encoded or decoded.|  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)