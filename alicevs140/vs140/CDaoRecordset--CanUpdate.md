---
title: "CDaoRecordset::CanUpdate"
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
ms.assetid: 7ff4d6b8-243b-4e5e-8ec7-fde909f468c2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::CanUpdate
Call this member function to determine whether the recordset can be updated.  
  
## Syntax  
  
```  
  
BOOL CanUpdate( ) const;  
  
```  
  
## Return Value  
 Nonzero if the recordset can be updated (add, update, and delete records), otherwise 0.  
  
## Remarks  
 A recordset might be read-only if the underlying data source is read-only or if you specified **dbReadOnly** for `nOptions` when you called [Open](../vs140/CDaoRecordset--Open.md) for the recordset.  
  
 For related information, see the topics "AddNew Method", "Edit Method", "Delete Method", "Update Method", and "Updatable Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::CanAppend](../vs140/CDaoRecordset--CanAppend.md)   
 [CDaoRecordset::CanBookmark](../vs140/CDaoRecordset--CanBookmark.md)   
 [CDaoRecordset::CanScroll](../vs140/CDaoRecordset--CanScroll.md)   
 [CDaoRecordset::CanRestart](../vs140/CDaoRecordset--CanRestart.md)   
 [CDaoRecordset::CanTransact](../vs140/CDaoRecordset--CanTransact.md)