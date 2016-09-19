---
title: "CWinApp::m_pszExeName"
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
ms.assetid: bc04e7c3-97dc-444e-bfa3-5fae75ba76e4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::m_pszExeName
Contains the name of the application's executable file without an extension.  
  
## Syntax  
  
```  
  
LPCTSTR m_pszExeName;  
  
```  
  
## Remarks  
 Unlike [m_pszAppName](../vs140/CWinApp--m_pszAppName.md), this name cannot contain blanks. `m_pszExeName` is a public variable of type **const char\***.  
  
> [!NOTE]
>  If you assign a value to `m_pszExeName`, it must be dynamically allocated on the heap. The `CWinApp` destructor calls **free**( ) with this pointer. You many want to use the `_tcsdup`( ) run-time library function to do the allocating. Also, free the memory associated with the current pointer before assigning a new value. For example:  
  
 [!CODE [NVC_MFCWindowing#58](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#58)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)