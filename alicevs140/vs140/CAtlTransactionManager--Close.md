---
title: "CAtlTransactionManager::Close"
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
ms.assetid: 072c2f53-b557-462f-9ac3-45eacf6e66b0
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTransactionManager::Close
Closes the transaction handle.  
  
## Syntax  
  
```  
inline BOOL CAtlTransactionManager::Close();  
```  
  
## Return Value  
 `TRUE` if successful; otherwise `FALSE`.  
  
## Remarks  
 This wrapper calls the `CloseHandle` function. The method is automatically called in the destructor.  
  
## Requirements  
 **Header:** atltransactionmanagerh  
  
## See Also  
 [CAtlTransactionManager Class](../vs140/CAtlTransactionManager-Class.md)