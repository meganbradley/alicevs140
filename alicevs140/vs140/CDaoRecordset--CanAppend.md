---
title: "CDaoRecordset::CanAppend"
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
ms.assetid: 030c9eb5-0f01-4120-acaa-0823ea1c2791
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::CanAppend
Call this member function to determine whether the previously opened recordset allows you to add new records by calling the [AddNew](../vs140/CDaoRecordset--AddNew.md) member function.  
  
## Syntax  
  
```  
  
BOOL CanAppend( ) const;  
  
```  
  
## Return Value  
 Nonzero if the recordset allows adding new records; otherwise 0. `CanAppend` will return 0 if you opened the recordset as read-only.  
  
## Remarks  
 For related information, see the topic "Append Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::CanBookmark](../vs140/CDaoRecordset--CanBookmark.md)   
 [CDaoRecordset::CanRestart](../vs140/CDaoRecordset--CanRestart.md)   
 [CDaoRecordset::CanScroll](../vs140/CDaoRecordset--CanScroll.md)   
 [CDaoRecordset::CanTransact](../vs140/CDaoRecordset--CanTransact.md)   
 [CDaoRecordset::CanUpdate](../vs140/CDaoRecordset--CanUpdate.md)