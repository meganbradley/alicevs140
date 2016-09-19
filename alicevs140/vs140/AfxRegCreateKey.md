---
title: "AfxRegCreateKey"
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
ms.assetid: 4c81e51c-9dfb-4358-a4c0-61dfe0eadf2d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxRegCreateKey
Creates the specified registry key.  
  
## Syntax  
  
```  
LONG AFXAPI AfxRegCreateKey(HKEY hKey, LPCTSTR lpSubKey, PHKEY phkResult, CAtlTransactionManager* pTM = NULL);  
```  
  
#### Parameters  
 `hKey`  
 A handle to an open registry key.  
  
 `lpSubKey`  
 The name of a key that this function opens or creates.  
  
 `phkResult`  
 A pointer to a variable that receives a handle to the opened or created key.  
  
 `pTM`  
 Pointer to a `CAtlTransactionManager` object.  
  
## Return Value  
 If the function succeeds, the return value is ERROR_SUCCESS. If the function fails, the return value is a nonzero error code defined in Winerror.h.  
  
## Remarks  
  
## Requirements  
 **Header:** afxpriv.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)