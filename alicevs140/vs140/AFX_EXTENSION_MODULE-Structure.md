---
title: "AFX_EXTENSION_MODULE Structure"
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
ms.assetid: b85a989c-d0c5-4b28-b53c-dad45b75704e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_EXTENSION_MODULE Structure
The `AFX_EXTENSION_MODULE` is used during initialization of MFC extension DLLs to hold the state of extension DLL module.  
  
## Syntax  
  
```  
  
      struct AFX_EXTENSION_MODULE  
{  
   BOOL bInitialized;  
   HMODULE hModule;  
   HMODULE hResource;  
   CRuntimeClass* pFirstSharedClass;  
   COleObjectFactory* pFirstSharedFactory;  
};  
```  
  
#### Parameters  
 *bInitialized*  
 **TRUE** if the DLL module has been initialized with `AfxInitExtensionModule`.  
  
 `hModule`  
 Specifies the handle of the DLL module.  
  
 *hResource*  
 Specifies the handle of the DLL custom resource module.  
  
 *pFirstSharedClass*  
 A pointer to information (the `CRuntimeClass` structure) about the DLL module's first runtime class. Used to provide the start of the runtime class list.  
  
 *pFirstSharedFactory*  
 A pointer to the DLL module's first object factory (a `COleObjectFactory` object). Used to provide the start of the class factory list.  
  
## Remarks  
 MFC extension DLLs need to do two things in their `DllMain` function:  
  
-   Call [AfxInitExtensionModule](../vs140/AfxInitExtensionModule.md) and check the return value.  
  
-   Create a **CDynLinkLibrary** object if the DLL will be exporting [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) objects or has its own custom resources.  
  
 The `AFX_EXTENSION_MODULE` structure is used to hold a copy of the extension DLL module state, including a copy of the runtime class objects that have been initialized by the extension DLL as part of normal static object construction executed before `DllMain` is entered. For example:  
  
 [!CODE [NVC_MFC_DLL#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_DLL#2)]  
  
 The module information stored in the `AFX_EXTENSION_MODULE` structure can be copied into the **CDynLinkLibrary** object. For example:  
  
 [!CODE [NVC_MFC_DLL#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_DLL#5)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Structures, Styles, Callbacks, and Message Maps](../vs140/Structures--Styles--Callbacks--and-Message-Maps.md)   
 [AfxInitExtensionModule](../vs140/AfxInitExtensionModule.md)   
 [AfxTermExtensionModule](../vs140/AfxTermExtensionModule.md)