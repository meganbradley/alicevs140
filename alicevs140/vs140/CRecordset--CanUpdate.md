---
title: "CRecordset::CanUpdate"
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
ms.assetid: 397dbf6d-305c-46f5-96c4-1b9822303557
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::CanUpdate
Determines whether the recordset can be updated.  
  
## Syntax  
  
```  
  
BOOL CanUpdate( ) const;  
```  
  
## Return Value  
 Nonzero if the recordset can be updated; otherwise 0.  
  
## Remarks  
 A recordset might be read-only if the underlying data source is read-only or if you specified **CRecordset::readOnly** in the `dwOptions` parameter when you opened the recordset.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::Open](../vs140/CRecordset--Open.md)   
 [CRecordset::AddNew](../vs140/CRecordset--AddNew.md)   
 [CRecordset::Edit](../vs140/CRecordset--Edit.md)   
 [CRecordset::Delete](../vs140/CRecordset--Delete.md)   
 [CRecordset::Update](../vs140/CRecordset--Update.md)