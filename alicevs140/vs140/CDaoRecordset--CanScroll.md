---
title: "CDaoRecordset::CanScroll"
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
ms.assetid: f685c0c3-7900-4c5e-8419-158612845632
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::CanScroll
Call this member function to determine whether the recordset allows scrolling.  
  
## Syntax  
  
```  
  
BOOL CanScroll( ) const;  
  
```  
  
## Return Value  
 Nonzero if you can scroll through the records, otherwise 0.  
  
## Remarks  
 If you call [Open](../vs140/CDaoRecordset--Open.md) with **dbForwardOnly**, the recordset can only scroll forward.  
  
 For related information, see the topic "Positioning the Current Record Pointer with DAO" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::CanAppend](../vs140/CDaoRecordset--CanAppend.md)   
 [CDaoRecordset::CanBookmark](../vs140/CDaoRecordset--CanBookmark.md)   
 [CDaoRecordset::CanRestart](../vs140/CDaoRecordset--CanRestart.md)   
 [CDaoRecordset::CanTransact](../vs140/CDaoRecordset--CanTransact.md)   
 [CDaoRecordset::CanUpdate](../vs140/CDaoRecordset--CanUpdate.md)   
 [CDaoRecordset::Open](../vs140/CDaoRecordset--Open.md)