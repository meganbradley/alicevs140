---
title: "AfxInitExtensionModule"
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
ms.assetid: 15f0c820-ff34-4da6-8077-79afbbb8dac1
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxInitExtensionModule
Call this function in an extension DLL's `DllMain` to initialize the DLL.  
  
## Syntax  
  
```  
  
      BOOL AFXAPI AfxInitExtensionModule(  
   AFX_EXTENSION_MODULE& state,  
   HMODULE hModule   
);  
```  
  
#### Parameters  
 `state`  
 A reference to the [AFX_EXTENSION_MODULE Structure](../vs140/AFX_EXTENSION_MODULE-Structure.md) structure that will contain the state of the extension DLL module after the initialization. The state includes a copy of the runtime class objects that have been initialized by the extension DLL as part of normal static object construction executed before `DllMain` is entered.  
  
 `hModule`  
 A handle of the extension DLL module.  
  
## Return Value  
 **TRUE** if the extension DLL is successfully initialized; otherwise, **FALSE**.  
  
## Remarks  
 For example:  
  
 [!CODE [NVC_MFC_DLL#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_DLL#2)]  
  
 `AfxInitExtensionModule` makes a copy of the DLL's **HMODULE** and captures the DLL's runtime-classes (`CRuntimeClass` structures) as well as its object factories (`COleObjectFactory` objects) for use later when the **CDynLinkLibrary** object is created.  
  
 MFC extension DLLs need to do two things in their `DllMain` function:  
  
-   Call [AfxInitExtensionModule](#_mfc_afxinitextensionmodule) and check the return value.  
  
-   Create a **CDynLinkLibrary** object if the DLL will be exporting [CRuntimeClass Structure](../vs140/CRuntimeClass-Structure.md) objects or has its own custom resources.  
  
 You can call `AfxTermExtensionModule` to clean up the extension DLL when each process detaches from the extension DLL (which happens when the process exits, or when the DLL is unloaded as a result of an `AfxFreeLibrary` call).  
  
## Requirements  
 **Header:** afxdll_.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxTermExtensionModule](../vs140/AfxTermExtensionModule.md)