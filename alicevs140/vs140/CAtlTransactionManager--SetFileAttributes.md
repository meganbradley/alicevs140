---
title: "CAtlTransactionManager::SetFileAttributes"
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
ms.assetid: 80266276-2b32-4764-9a99-1513530187f1
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTransactionManager::SetFileAttributes
Sets the attributes for a file or directory as a transacted operation.  
  
## Syntax  
  
```  
inline BOOL CAtlTransactionManager::SetFileAttributes(  
   LPCTSTR lpFileName,  
   DWORD dwAttributes  
);  
```  
  
#### Parameters  
 `lpFileName`  
 The name of the file or directory.  
  
 `dwAttributes`  
 The file attributes to set for the file. For more information, see [SetFileAttributesTransacted](http://go.microsoft.com/fwlink/?LinkId=158699).  
  
## Remarks  
 This wrapper calls the `SetFileAttributesTransacted` function.  
  
## Requirements  
 **Header:** atltransactionmanager.h  
  
## See Also  
 [CAtlTransactionManager Class](../vs140/CAtlTransactionManager-Class.md)