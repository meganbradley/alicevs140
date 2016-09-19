---
title: "CWinApp::m_pszAppName"
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
ms.topic: reference
ms.assetid: f0f7ff5c-176a-4c8a-9fb8-889fce314718
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::m_pszAppName
Specifies the name of the application.  
  
## Syntax  
  
```  
  
LPCTSTR m_pszAppName;  
  
```  
  
## Remarks  
 The application name can come from the parameter passed to the [CWinApp](../vs140/CWinApp--CWinApp.md) constructor, or, if not specified, to the resource string with the ID of **AFX_IDS_APP_TITLE**. If the application name is not found in the resource, it comes from the program's .EXE filename.  
  
 Returned by the global function [AfxGetAppName](../vs140/AfxGetAppName.md). `m_pszAppName` is a public variable of type **const char\***.  
  
> [!NOTE]
>  If you assign a value to `m_pszAppName`, it must be dynamically allocated on the heap. The `CWinApp` destructor calls **free**( ) with this pointer. You many want to use the `_tcsdup`( ) run-time library function to do the allocating. Also, free the memory associated with the current pointer before assigning a new value. For example:  
  
 [!CODE [NVC_MFCWindowing#57](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#57)]  
  
## Example  
 [!CODE [NVC_MFCWindowing#65](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#65)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)