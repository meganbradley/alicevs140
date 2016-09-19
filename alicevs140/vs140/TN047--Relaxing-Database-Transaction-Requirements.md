---
title: "TN047: Relaxing Database Transaction Requirements"
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
ms.assetid: f93c51cf-a8c0-43d0-aa47-7bcb8333d693
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# TN047: Relaxing Database Transaction Requirements
This tech note, which discussed the transaction requirements of the MFC ODBC database classes, is now obsolete. Before MFC 4.2, the database classes required that cursors be preserved on recordsets after a **CommitTrans** or **Rollback** operation. If the ODBC driver and DBMS did not support this level of cursor preservation, then the database classes did not enable transactions.  
  
 Beginning with MFC 4.2, the database classes have relaxed the restriction of requiring cursor preservation. Transactions will be enabled if the driver supports them. However, you must now check the effect of a **CommitTrans** or **Rollback** operation on open recordsets. See the member functions [CDatabase::GetCursorCommitBehavior](../vs140/CDatabase--GetCursorCommitBehavior.md) and [CDatabase::GetCursorRollbackBehavior](../vs140/CDatabase--GetCursorRollbackBehavior.md) for more information.  
  
## See Also  
 [Technical Notes by Number](../vs140/Technical-Notes-by-Number.md)   
 [Technical Notes by Category](../vs140/Technical-Notes-by-Category.md)