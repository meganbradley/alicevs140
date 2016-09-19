---
title: "AfxGetInstanceHandle"
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
ms.assetid: 3a2c97b9-e65c-4921-8f62-c7045f867732
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxGetInstanceHandle
This function allows you to retrieve the instance handle of the current application.  
  
## Syntax  
  
```  
  
HINSTANCE AFXAPI AfxGetInstanceHandle( );  
```  
  
## Return Value  
 An `HINSTANCE` to the current instance of the application. If called from within a DLL linked with the USRDLL version of MFC, an `HINSTANCE` to the DLL is returned.  
  
## Remarks  
 `AfxGetInstanceHandle` always returns the `HINSTANCE` of your executable file (.EXE) unless it is called from within a DLL linked with the USRDLL version of MFC. In this case, it returns an `HINSTANCE` to the DLL.  
  
## Example  
 [!CODE [NVC_MFCWindowing#128](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#128)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxGetResourceHandle](../vs140/AfxGetResourceHandle.md)   
 [AfxSetResourceHandle](../vs140/AfxSetResourceHandle.md)