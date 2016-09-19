---
title: "CRecordset::GetRecordCount"
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
ms.assetid: edc3ab82-6245-46d5-bc84-544f7bba1d3b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::GetRecordCount
Determines the size of the recordset.  
  
## Syntax  
  
```  
  
long GetRecordCount( ) const;  
```  
  
## Return Value  
 The number of records in the recordset; 0 if the recordset contains no records; or –1 if the record count cannot be determined.  
  
## Remarks  
  
> [!CAUTION]
>  The record count is maintained as a "high water mark," the highest-numbered record yet seen as the user moves through the records. The total number of records is only known after the user has moved beyond the last record. For performance reasons, the count is not updated when you call `MoveLast`. To count the records yourself, call `MoveNext` repeatedly until `IsEOF` returns nonzero. Adding a record via **CRecordset:AddNew** and **Update** increases the count; deleting a record via `CRecordset::Delete` decreases the count.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::MoveLast](../vs140/CRecordset--MoveLast.md)   
 [CRecordset::MoveNext](../vs140/CRecordset--MoveNext.md)   
 [CRecordset::IsEOF](../vs140/CRecordset--IsEOF.md)   
 [CRecordset::GetStatus](../vs140/CRecordset--GetStatus.md)