---
title: "AfxNetInitModule"
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
ms.assetid: 5593eacd-c62e-4baf-87a8-60819702494b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxNetInitModule
For MFC Sockets support from a regular DLL that is dynamically linked to MFC, add a call to this function in your regular DLL's **CWinApp::InitInstance** function to initialize the MFC Sockets DLL.  
  
## Syntax  
  
```  
  
void AFXAPI AfxNetInitModule( );  
```  
  
## Remarks  
 The MFC Sockets DLL is an extension DLL; in order for an extension DLL to get wired into a **CDynLinkLibrary** chain, it must create a **CDynLinkLibrary** object in the context of every module that will be using it. `AfxNetInitModule` creates the **CDynLinkLibrary** object in your regular DLL's context so that it gets wired into the **CDynLinkLibrary** object chain of the regular DLL.  
  
## Requirements  
 **Header:** <afxdll_.h>  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxMessageBox](../vs140/AfxMessageBox.md)