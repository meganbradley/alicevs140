---
title: "CAtlTransactionManager::MoveFile"
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
ms.assetid: 4811a415-0708-49c5-a4b2-620be697a606
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTransactionManager::MoveFile
Moves an existing file or a directory, including its children, as a transacted operation.  
  
## Syntax  
  
```  
inline BOOL CAtlTransactionManager::MoveFile(  
   LPCTSTR lpOldFileName,  
   LPCTSTR lpNewFileName  
);  
```  
  
#### Parameters  
 `lpOldFileName`  
 The current name of the existing file or directory on the local computer.  
  
 `lpNewFileName`  
 The new name for the file or directory. This name must not already exist. A new file may be on a different file system or drive. A new directory must be on the same drive.  
  
## Remarks  
 This wrapper calls the `MoveFileTransacted` function.  
  
## Requirements  
 **Header:** atltransactionmanager.h  
  
## See Also  
 [CAtlTransactionManager Class](../vs140/CAtlTransactionManager-Class.md)