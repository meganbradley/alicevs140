---
title: "JScript Functions for C++ Wizards"
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
ms.assetid: f3046c56-cf67-4aaa-919e-8c066bfb6760
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# JScript Functions for C++ Wizards
|||  
|-|-|  
|[AddATLSupportToProject](../vs140/AddATLSupportToProject.md)|Adds ATL support to an MFC project.|  
|[AddCoclassFromFile](../vs140/AddCoclassFromFile.md)|Renders and inserts into the project's .idl file a template file that contains a coclass.|  
|[AddCommonConfig](../Topic/AddCommonConfig.md)|Adds the default configurations to the project.|  
|[AddFilesToProject](../vs140/AddFilesToProject.md)|Adds all the files to the project based on the list in the file Templates.inf.|  
|[AddInterfaceFromFile](../vs140/AddInterfaceFromFile.md)|Renders and inserts into the project's IDL file a template file that contains an interface.|  
|[CanAddATLClass](../vs140/CanAddATLClass.md)|Called by the wizard to verify if the project is compatible with the code wizard that is about to be run (in other words, it can accept an ATL class).<br /><br /> The wizard calls this function when the parameter PREPROCESS_FUNCTION is in the [project control's .vsz file](../Topic/.Vsz%20File%20\(Project%20Control\).md) and checks if the [Visual C++ Code Model](assetId:///dd6452c2-1054-44a1-b0eb-639a94a1216b) is available. If the code model is not available, the function reports an error and returns **false**.|  
|[CanAddClass](../vs140/CanAddClass.md)|The wizard calls this function when the parameter PREPROCESS_FUNCTION is in the project control's .vsz file.<br /><br /> It verifies if the Visual C++ Code Model object is available. If the code model is not available, the function reports an error and returns **false**.|  
|[CanAddMFCClass](../vs140/CanAddMFCClass.md)|Called by the wizard to verify if the project is compatible with the Code Wizard that is about to be run (in other words, it can accept an MFC class).<br /><br /> The wizard calls this function when the parameter PREPROCESS_FUNCTION is in the project control's .vsz file and checks if the Visual C++ Code Model object is available. If the code model is not available, the function reports an error and returns **false**.|  
|[CanAddNonAttributed](../vs140/CanAddNonAttributed.md)|Indicates whether the project supports both attributed and nonattributed ATL objects.|  
|[CanUseFileName](../vs140/CanUseFileName.md)|Checks if a file exists. If so, the wizard prompts the user to merge the code to be added to the existing file.|  
|[ConvertProjectToAttributed](../vs140/ConvertProjectToAttributed.md)|Converts an ATL project to attributed.|  
|[CreateInfFile](../vs140/CreateInfFile.md)|Creates the Templates.inf file.|  
|[CreateProject](../vs140/CreateProject.md)|Creates a C++ project.|  
|[CreateSafeName](../vs140/CreateSafeName.md)|Generates a C++ friendly name.|  
|[DeleteFile](../vs140/DeleteFile.md)|Deletes the specified file.|  
|[DoesIncludeExist](../vs140/DoesIncludeExist.md)|Indicates whether a `#include` statement exists in a file.|  
|[GetCodeForDllCanUnloadNow](../vs140/GetCodeForDllCanUnloadNow.md)|Retrieves code needed to unload the DLL.|  
|[GetCodeForDllGetClassObject](../vs140/GetCodeForDllGetClassObject.md)|Retrieves the code for the DLL class object.|  
|[GetCodeForDllRegisterServer](../vs140/GetCodeForDllRegisterServer.md)|Retrieves the code to register a server.|  
|[GetCodeForDllUnregisterServer](../vs140/GetCodeForDllUnregisterServer.md)|Retrieves the code to unregister a server.|  
|[GetCodeForExitInstance](../vs140/GetCodeForExitInstance.md)|Helper function to get the text for `ExitInstance`.|  
|[GetCodeForInitInstance](../vs140/GetCodeForInitInstance.md)|Helper function to get the text for [InitInstance](../vs140/CWinApp--InitInstance.md).|  
|[GetExportPragmas](../vs140/GetExportPragmas.md)|Retrieves the pragmas for exporting functions.|  
|[GetInterfaceClasses](../vs140/GetInterfaceClasses.md)|Returns the `VCCodeClass` object associated with an interface.|  
|[GetInterfaceType](../vs140/GetInterfaceType.md)|Returns the type of interface (for example, custom, dual, dispinterface, oleautomation).|  
|[GetMaxID](../Topic/GetMaxID.md)|Returns the highest `dispid` from members of this interface and all of its bases.|  
|[GetMemberfunction](../vs140/GetMemberfunction.md)|Returns a function object based on the given name.|  
|[GetProjectFile](../vs140/GetProjectFile.md)|Returns the file name of per-project type of files (.rc, .idl, and so on).|  
|[GetProjectPath](../vs140/GetProjectPath.md)|Returns the project's directory path.|  
|[GetRuntimeErrorDesc](../vs140/GetRuntimeErrorDesc.md)|Returns a description for the type of exception.|  
|[GetUniqueFileName](../vs140/GetUniqueFileName.md)|Returns a unique file name.|  
|[IncludeCodeElementDeclaration](../vs140/IncludeCodeElementDeclaration.md)|Adds the include statement to `strInFile`, including the header where `strCodeElemName` is implemented, if such a header found is in the project.|  
|[InsertIntoFunction](../vs140/InsertIntoFunction.md)|Helper function called in `AddATLSupportToProject` to insert code into `InitInstance`.|  
|[IsATLProject](../vs140/IsATLProject.md)|Indicates whether project is ATL based.|  
|[IsAttributedProject](../vs140/IsAttributedProject.md)|Indicates whether a project is attributed.|  
|[IsMFCProject](../vs140/IsMFCProject.md)|Checks if a project is MFC based.|  
|[LineBeginsWith](../vs140/LineBeginsWith.md)|Helper function called in `InsertIntoFunction` to determine if a line begins with a particular string|  
|[OffsetToLineNumber](../vs140/OffsetToLineNumber.md)|Finds the line number for a given position in a function body.|  
|[OnWizFinish](../vs140/OnWizFinish.md)|Called from the wizard HTML script when the user clicks **Finish**. Calls the wizard control's **Finish** method.|  
|[RenderAddTemplate](../vs140/RenderAddTemplate.md)|Renders a template file and optionally adds it to the project.|  
|[SetCommonPchSettings](../vs140/SetCommonPchSettings.md)|Sets up the precompiled header for the project.|  
|[SetErrorInfo](../vs140/SetErrorInfo.md)|Provides error information.|  
|[SetFilters](../vs140/SetFilters.md)|Adds source, include, and resource filters for project folders.|  
|[SetMergeProxySymbol](../vs140/SetMergeProxySymbol.md)|Called by the wizard to add the _MERGE_PROXYSTUB symbol if needed.|  
|[SetNoPchSettings](../vs140/SetNoPchSettings.md)|Sets up the project configuration properties when no precompiled header is used.|  
  
## See Also  
 [Customizing C++ Wizards with Common JScript Functions](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)