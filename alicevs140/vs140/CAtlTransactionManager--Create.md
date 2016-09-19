---
title: "CAtlTransactionManager::Create"
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
ms.assetid: c23a07c7-d519-4da5-a27a-b878e9c93a9a
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTransactionManager::Create
Creates the transaction handle.  
  
## Syntax  
  
```  
inline BOOL CAtlTransactionManager::Create();  
```  
  
## Return Value  
 `TRUE` if successful; otherwise `FALSE`.  
  
## Remarks  
 This wrapper calls the `CreateTransaction` function. Check it for  
  
## Requirements  
 **Header:** atltransactionmanager.h  
  
## See Also  
 [CAtlTransactionManager Class](../vs140/CAtlTransactionManager-Class.md)