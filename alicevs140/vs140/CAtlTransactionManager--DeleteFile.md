---
title: "CAtlTransactionManager::DeleteFile"
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
ms.assetid: a6ff1c0d-5f18-4363-b91e-04620b6a545b
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTransactionManager::DeleteFile
Deletes an existing file as a transacted operation.  
  
## Syntax  
  
```  
inline BOOL CAtlTransactionManager::DeleteFile(  
   LPCTSTR lpFileName  
);  
```  
  
#### Parameters  
 `lpFileName`  
 The name of the file to be deleted.  
  
## Remarks  
 This wrapper calls the `DeleteFileTransacted` function.  
  
## Requirements  
 **Header:** atltransactionmanager.h  
  
## See Also  
 [CAtlTransactionManager Class](../vs140/CAtlTransactionManager-Class.md)