---
title: "CAtlTransactionManager::GetFileAttributes"
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
ms.assetid: f82ab29b-0e57-42d8-b477-8edec5429d5f
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTransactionManager::GetFileAttributes
Retrieves file system attributes for a specified file or directory as a transacted operation.  
  
## Syntax  
  
```  
inline DWORD CAtlTransactionManager::GetFileAttributes(  
   LPCTSTR lpFileName  
);  
```  
  
#### Parameters  
 `lpFileName`  
 The name of the file or directory.  
  
## Remarks  
 This wrapper calls the `GetFileAttributesTransacted` function.  
  
## Requirements  
 **Header:** atltransactionmanager.h  
  
## See Also  
 [CAtlTransactionManager Class](../vs140/CAtlTransactionManager-Class.md)