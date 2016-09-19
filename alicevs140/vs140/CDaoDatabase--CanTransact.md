---
title: "CDaoDatabase::CanTransact"
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
ms.assetid: 2773b162-245f-4632-8966-0e99a7acc32a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::CanTransact
Call this member function to determine whether the database allows transactions.  
  
## Syntax  
  
```  
  
BOOL CanTransact( );  
  
```  
  
## Return Value  
 Nonzero if the database supports transactions; otherwise 0.  
  
## Remarks  
 Transactions are managed in the database's workspace.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoWorkspace::BeginTrans](../vs140/CDaoWorkspace--BeginTrans.md)   
 [CDaoWorkspace::CommitTrans](../vs140/CDaoWorkspace--CommitTrans.md)   
 [CDaoWorkspace::Rollback](../vs140/CDaoWorkspace--Rollback.md)