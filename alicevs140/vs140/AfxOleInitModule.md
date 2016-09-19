---
title: "AfxOleInitModule"
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
ms.assetid: c19bf8ed-f398-4cd0-b23f-6ef379485403
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxOleInitModule
For OLE support from a regular DLL that is dynamically linked to MFC, call this function in your regular DLL's `CWinApp::InitInstance` function to initialize the MFC OLE DLL.  
  
## Syntax  
  
```  
  
void AFXAPI AfxOleInitModule( );  
```  
  
## Remarks  
 The MFC OLE DLL is an extension DLL; in order for an extension DLL to get wired into a **CDynLinkLibrary** chain, it must create a **CDynLinkLibrary** object in the context of every module that will be using it. `AfxOleInitModule` creates the **CDynLinkLibrary** object in your regular DLL's context so that it gets wired into the **CDynLinkLibrary** object chain of the regular DLL.  
  
 If you are building an OLE control and are using `COleControlModule`, you should not call **AfxOleInitModule** because the `InitInstance` member function for `COleControlModule` calls `AfxOleInitModule`.  
  
## Requirements  
 **Header**: <afxdll_.h>  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxMessageBox](../vs140/AfxMessageBox.md)