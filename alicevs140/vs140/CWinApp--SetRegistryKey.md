---
title: "CWinApp::SetRegistryKey"
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
ms.assetid: a4df20ef-2e90-4040-a06d-0cfb27e34d70
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::SetRegistryKey
Causes application settings to be stored in the registry instead of INI files.  
  
## Syntax  
  
```  
  
      void SetRegistryKey(  
   LPCTSTR lpszRegistryKey   
);  
void SetRegistryKey(  
   UINT nIDRegistryKey   
);  
```  
  
#### Parameters  
 *lpszRegistryKey*  
 Pointer to a string containing the name of the key.  
  
 *nIDRegistryKey*  
 ID of a string resource containing the name of the registry key.  
  
## Remarks  
 This function sets *m_pszRegistryKey*, which is then used by the `GetProfileInt`, `GetProfileString`, `WriteProfileInt`, and `WriteProfileString` member functions of `CWinApp`. If this function has been called, the list of most recently-used (MRU) files is also stored in the registry. The registry key is usually the name of a company. It is stored in a key of the following form: HKEY_CURRENT_USER\Software\\<company name\>\\<application name\>\\<section name\>\\<value name\>.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md)   
 [CWinApp::GetProfileInt](../vs140/CWinApp--GetProfileInt.md)   
 [CWinApp::GetProfileString](../vs140/CWinApp--GetProfileString.md)   
 [CWinApp::WriteProfileInt](../vs140/CWinApp--WriteProfileInt.md)   
 [CWinApp::WriteProfileString](../vs140/CWinApp--WriteProfileString.md)