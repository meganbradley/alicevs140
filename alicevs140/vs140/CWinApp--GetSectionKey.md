---
title: "CWinApp::GetSectionKey"
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
ms.assetid: 591f75b6-6393-41ad-b891-9791e9ee31ae
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::GetSectionKey
Returns the key for HKEY_CURRENT_USER\\"Software"\RegistryKey\AppName\lpszSection.  
  
## Syntax  
  
```  
HKEY GetSectionKey(  
   LPCTSTR lpszSection,  
   CAtlTransactionManager* pTM = NULL  
);  
```  
  
#### Parameters  
 `lpszSection`  
 The name of the key to be obtained.  
  
 `pTM`  
 Pointer to a `CAtlTransactionManager` object.  
  
## Return Value  
 Section key if the function succeeds; otherwise `NULL`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)