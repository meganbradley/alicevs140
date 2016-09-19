---
title: "CWinApp::m_pszProfileName"
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
ms.assetid: 53f35c1f-b7f9-45f2-a8d9-556b4a1b9f91
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::m_pszProfileName
Contains the name of the application's .INI file.  
  
## Syntax  
  
```  
  
LPCTSTR m_pszProfileName;  
  
```  
  
## Remarks  
 `m_pszProfileName` is a public variable of type **const char\***.  
  
> [!NOTE]
>  If you assign a value to `m_pszProfileName`, it must be dynamically allocated on the heap. The `CWinApp` destructor calls **free**( ) with this pointer. You many want to use the `_tcsdup`( ) run-time library function to do the allocating. Also, free the memory associated with the current pointer before assigning a new value. For example:  
  
 [!CODE [NVC_MFCWindowing#60](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#60)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::GetProfileString](../vs140/CWinApp--GetProfileString.md)   
 [CWinApp::GetProfileInt](../vs140/CWinApp--GetProfileInt.md)   
 [CWinApp::WriteProfileInt](../vs140/CWinApp--WriteProfileInt.md)   
 [CWinApp::WriteProfileString](../vs140/CWinApp--WriteProfileString.md)