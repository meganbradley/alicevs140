---
title: "AfxGetApp"
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
ms.assetid: dd869fe6-157c-4317-a624-1e92830d7f83
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxGetApp
The pointer returned by this function can be used to access application information such as the main message-dispatch code or the topmost window.  
  
## Syntax  
  
```  
  
CWinApp* AFXAPI AfxGetApp( );   
```  
  
## Return Value  
 A pointer to the single `CWinApp` object for the application.  
  
## Remarks  
 If this method returns NULL, it might indicate that the application’s main window has not been fully initialized yet. It might also indicate a problem.  
  
## Example  
 [!CODE [NVC_MFCWindowing#126](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#126)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)