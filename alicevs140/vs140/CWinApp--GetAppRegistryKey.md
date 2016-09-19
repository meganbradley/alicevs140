---
title: "CWinApp::GetAppRegistryKey"
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
ms.assetid: 451162d3-7941-4fe8-ba5e-1a37d1c5d666
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::GetAppRegistryKey
Returns the key for HKEY_CURRENT_USER\\"Software"\RegistryKey\ProfileName.  
  
## Syntax  
  
```  
HKEY GetAppRegistryKey(  
   CAtlTransactionManager* pTM = NULL  
);  
```  
  
#### Parameters  
 `pTM`  
 Pointer to a `CAtlTransactionManager` object.  
  
## Return Value  
 Application key if the function succeeds; otherwise `NULL`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)