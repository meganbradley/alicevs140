---
title: "CAtlTransactionManager::FindFirstFile"
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
ms.assetid: 44b9514e-3aeb-41f8-853a-b38f992bc695
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTransactionManager::FindFirstFile
Searches a directory for a file or subdirectory as a transacted operation.  
  
## Syntax  
  
```  
inline HANDLE CAtlTransactionManager::FindFirstFile(  
   LPCTSTR lpFileName,  
   WIN32_FIND_DATA* pNextInfo  
);  
```  
  
#### Parameters  
 `lpFileName`  
 The directory or path, and the file name to search for. This parameter can include wildcard characters, such as an asterisk (*) or a question mark (?).  
  
 `pNextInfo`  
 A pointer to the WIN32_FIND_DATA structure that receives information about a found file or subdirectory.  
  
## Return Value  
 If the function succeeds, the return value is a search handle used in a subsequent call to `FindNextFile` or `FindClose`. If the function fails or fails to locate files from the search string in the `lpFileName` parameter, the return value is INVALID_HANDLE_VALUE.  
  
## Remarks  
 This wrapper calls the `FindFirstFileTransacted` function.  
  
## Requirements  
 **Header:** atltransactionmanager.h  
  
## See Also  
 [CAtlTransactionManager Class](../vs140/CAtlTransactionManager-Class.md)