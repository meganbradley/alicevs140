---
title: "CWinApp::m_pszRegistryKey"
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
ms.assetid: 498ae5af-a88b-4f6c-99e9-628ff6af619d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::m_pszRegistryKey
Used to determine where, in the registry or INI file, application profile settings are stored.  
  
## Syntax  
  
```  
  
LPCTSTR m_pszRegistryKey;  
```  
  
## Remarks  
 Normally, this data member is treated as read-only.  
  
-   The value is stored to a registry key. The name for the application profile setting is appended to the following registry key: HKEY_CURRENT_USER/Software/LocalAppWizard-Generated/.  
  
 If you assign a value to `m_pszRegistryKey`, it must be dynamically allocated on the heap. The `CWinApp` destructor calls **free**( ) with this pointer. You many want to use the `_tcsdup`( ) run-time library function to do the allocating. Also, free the memory associated with the current pointer before assigning a new value. For example:  
  
 [!CODE [NVC_MFCWindowing#61](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#61)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::SetRegistryKey](../vs140/CWinApp--SetRegistryKey.md)