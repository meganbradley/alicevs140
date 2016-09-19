---
title: "AfxTermExtensionModule"
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
ms.assetid: b64de402-f1e3-4c26-9823-08c07876aaaa
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxTermExtensionModule
Call this function to allow MFC to cleanup the extension DLL when each process detaches from the DLL (which happens when the process exits, or when the DLL is unloaded as a result of a `AfxFreeLibrary` call).  
  
## Syntax  
  
```  
  
      void AFXAPI AfxTermExtensionModule(  
   AFX_EXTENSION_MODULE& state,  
   BOOL bAll  = FALSE   
);  
```  
  
#### Parameters  
 `state`  
 A reference to the [AFX_EXTENSION_MODULE](../vs140/AFX_EXTENSION_MODULE-Structure.md) structure that contains the state of extension DLL module.  
  
 *bAll*  
 If **TRUE**, cleanup all extension DLL modules. Otherwise, cleanup only the current DLL module.  
  
## Remarks  
 `AfxTermExtensionModule` will delete any local storage attached to the module and remove any entries from the message map cache. For example:  
  
 [!CODE [NVC_MFC_DLL#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_DLL#4)]  
  
 If your application loads and frees extension DLLs dynamically, be sure to call `AfxTermExtensionModule`. Since most extension DLLs are not dynamically loaded (usually, they are linked via their import libraries), the call to `AfxTermExtensionModule` is usually not necessary.  
  
 MFC extension DLLs need to call [AfxInitExtensionModule](../vs140/AfxInitExtensionModule.md) in their `DllMain`. If the DLL will be exporting [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) objects or has its own custom resources, you also need to create a **CDynLinkLibrary** object in `DllMain`.  
  
## Requirements  
 **Header:** afxdll_.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxInitExtensionModule](../vs140/AfxInitExtensionModule.md)