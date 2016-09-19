---
title: "CAtlTransactionManager::GetFileAttributesEx"
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
ms.assetid: 1271f497-5668-49a6-bf6e-dba7a5697abd
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTransactionManager::GetFileAttributesEx
Retrieves file system attributes for a specified file or directory as a transacted operation.  
  
## Syntax  
  
```  
inline BOOL CAtlTransactionManager::GetFileAttributesEx(  
   LPCTSTR lpFileName,  
   GET_FILEEX_INFO_LEVELS fInfoLevelId,  
   LPVOID lpFileInformation  
);  
```  
  
#### Parameters  
 `lpFileName`  
 The name of the file or directory.  
  
 `fInfoLevelId`  
 The level of attribute information to retrieve.  
  
 `lpFileInformation`  
 A pointer to a buffer that receives the attribute information. The type of attribute information that is stored into this buffer is determined by the value of `fInfoLevelId`. If the `fInfoLevelId` parameter is GetFileExInfoStandard then this parameter points to a WIN32_FILE_ATTRIBUTE_DATA structure.  
  
## Remarks  
 This wrapper calls the `GetFileAttributesTransacted` function.  
  
## Requirements  
 **Header:** atltransactionmanager.h  
  
## See Also  
 [CAtlTransactionManager Class](../vs140/CAtlTransactionManager-Class.md)