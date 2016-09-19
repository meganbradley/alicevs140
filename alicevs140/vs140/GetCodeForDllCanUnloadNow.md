---
title: "GetCodeForDllCanUnloadNow"
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
ms.assetid: 24ee3ef7-45be-4778-99e8-6df493f0782b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetCodeForDllCanUnloadNow
Gets the appropriate code for unloading the DLL.  
  
## Syntax  
  
```  
  
      function GetCodeForDllCanUnloadNow(   
   nLineStart,   
   nLineEnd    
);  
```  
  
#### Parameters  
 `nLineStart`  
 The zero-based line number for the start of the function.  
  
 `nLineEnd`  
 The zero-based line number for the end of the function.  
  
## Return Value  
 A string containing the code for unloading the DLL.  
  
## Remarks  
 Call this member function to retrieve the appropriate code for unloading the DLL. Calling this function creates a single string by concatenating the array elements you specify.  
  
 The following table shows code for unloading the DLL.  
  
|Line number|Code|  
|-----------------|----------|  
|0|AFX_MANAGE_STATE(AfxGetStaticModuleState());|  
|1|if (_AtlModule.GetLockCount() > 0)|  
|2|\treturn S_FALSE;|  
|3|return S_OK;|  
  
 For each of the lines returned, `GetCodeForDllCanUnloadNow` adds a leading tab (`\t`) and a trailing "CR-LF" (carriage return - linefeed) character pair (`\r\n`).  
  
## Example  
  
```  
// Get the lines numbered 1 and 2 above  
GetCodeForDllCanUnloadNow(1, 2)  
  
// returns the following string  
// "\tif (_AtlModule.GetLockCount() > 0)\r\n\t\treturn S_FALSE;\r\n"  
  
```  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)   
 [GetCodeForDllGetClassObject](../vs140/GetCodeForDllGetClassObject.md)   
 [GetCodeForExitInstance](../vs140/GetCodeForExitInstance.md)