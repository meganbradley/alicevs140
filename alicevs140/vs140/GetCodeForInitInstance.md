---
title: "GetCodeForInitInstance"
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
ms.assetid: cfa4cb9f-d1cc-4be6-8db9-c253655b57e4
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetCodeForInitInstance
Retrieves the specified code for [InitInstance](../vs140/CWinApp--InitInstance.md).  
  
## Syntax  
  
```  
  
      function GetCodeForInitInstance(   
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
 A string containing the code for initializing the wizard instance.  
  
## Remarks  
 Call this member function to retrieve the appropriate code for initializing the wizard instance. The line numbers are as follows:  
  
|Line number|InitInstance Code|  
|-----------------|-----------------------|  
|0|`CWinApp::InitInstance();`|  
|1|`return TRUE;`|  
|2|`AfxOleInit();`|  
|3|`// Parse command line for standard shell commands, DDE, file open`|  
|4|`CCommandLineInfo cmdInfo;`|  
|5|`ParseCommandLine(cmdInfo);`|  
|6|`// App was launched with /Embedding or /Automation switch.`|  
|7|`// Run app as automation server.`|  
|8|`if (cmdInfo.m_bRunEmbedded &#124;&#124; cmdInfo.m_bRunAutomated)`|  
|9|`{`|  
|10|`\t// Register class factories via CoRegisterClassObject().`|  
|11|`\tif (FAILED(_AtlModule.RegisterClassObjects(CLSCTX_LOCAL_SERVER, REGCLS_MULTIPLEUSE)))`|  
|12|`\t\treturn FALSE;`|  
|13|`\t// Don't show the main window`|  
|14|`\treturn TRUE;`|  
|15|`}`|  
|16|`// App was launched with /Unregserver or /Unregister switch.`|  
|17|`if (cmdInfo.m_nShellCommand == CCommandLineInfo::AppUnregister)`|  
|18|`{`|  
|19|`\t_AtlModule.UpdateRegistryAppId(FALSE);`|  
|20|`\t_AtlModule.UnregisterServer(TRUE);`|  
|21|`\treturn FALSE;`|  
|22|`}`|  
|23|`// App was launched with /Register or /Regserver switch.`|  
|24|`if (cmdInfo.m_nShellCommand == CCommandLineInfo::AppRegister)`|  
|25|`{`|  
|26|`\t_AtlModule.UpdateRegistryAppId(TRUE);`|  
|27|`\t_AtlModule.RegisterServer(TRUE);`|  
|28|`\treturn FALSE;`|  
|29|`}`|  
  
 For each of the lines returned, `GetCodeForInitInstance` adds a leading tab (`\t`) and a trailing "CR-LF" (carriage return - linefeed) character pair (`\r\n`).  
  
## Example  
  
```  
// Get the lines numbered 0 through 2 above  
GetCodeForInitInstance(0, 2)  
  
// returns the following string  
// "\tCWinApp::InitInstance();\r\n\treturn TRUE;\r\n\tAfxOleInit();\r\n"  
  
```  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [JScript Functions for C++ Wizards](../vs140/JScript-Functions-for-C---Wizards.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)   
 [GetCodeForExitInstance](../vs140/GetCodeForExitInstance.md)