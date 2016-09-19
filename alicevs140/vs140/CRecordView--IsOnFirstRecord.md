---
title: "CRecordView::IsOnFirstRecord"
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
ms.assetid: b5185382-1422-405d-aaec-cb37efcd26a4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordView::IsOnFirstRecord
Call this member function to determine whether the current record is the first record in the recordset object associated with this record view.  
  
## Syntax  
  
```  
  
BOOL IsOnFirstRecord( );  
```  
  
## Return Value  
 Nonzero if the current record is the first record in the recordset; otherwise 0.  
  
## Remarks  
 This function is useful for writing your own implementations of default command update handlers written by ClassWizard.  
  
 If the user moves to the first record, the framework disables any user interface objects you have for moving to the first or the previous record.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordView Class](../vs140/CRecordView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordView::OnMove](../vs140/CRecordView--OnMove.md)   
 [CRecordView::IsOnLastRecord](../vs140/CRecordView--IsOnLastRecord.md)   
 [CRecordset::IsBOF](../vs140/CRecordset--IsBOF.md)   
 [CRecordset::GetRecordCount](../vs140/CRecordset--GetRecordCount.md)