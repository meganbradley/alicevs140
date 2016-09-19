---
title: "CDaoRecordset::CanTransact"
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
ms.assetid: e1465fd6-4467-4962-ad32-ab9490d1ca28
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::CanTransact
Call this member function to determine whether the recordset allows transactions.  
  
## Syntax  
  
```  
  
BOOL CanTransact( );  
  
```  
  
## Return Value  
 Nonzero if the underlying data source supports transactions, otherwise 0.  
  
## Remarks  
 For related information, see the topic "Transactions Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::AddNew](../vs140/CDaoRecordset--AddNew.md)   
 [CDaoRecordset::CanAppend](../vs140/CDaoRecordset--CanAppend.md)   
 [CDaoRecordset::CancelUpdate](../vs140/CDaoRecordset--CancelUpdate.md)   
 [CDaoRecordset::CanScroll](../vs140/CDaoRecordset--CanScroll.md)   
 [CDaoRecordset::CanRestart](../vs140/CDaoRecordset--CanRestart.md)   
 [CDaoRecordset::CanUpdate](../vs140/CDaoRecordset--CanUpdate.md)   
 [CDaoRecordset::Delete](../vs140/CDaoRecordset--Delete.md)   
 [CDaoRecordset::Edit](../vs140/CDaoRecordset--Edit.md)   
 [CDaoRecordset::Update](../vs140/CDaoRecordset--Update.md)