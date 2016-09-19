---
title: "CRecordset::IsEOF"
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
ms.assetid: 5801f1ad-b71a-4b1a-8e42-40abed92a21c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::IsEOF
Returns nonzero if the recordset has been positioned after the last record. There is no current record.  
  
## Syntax  
  
```  
  
BOOL IsEOF( ) const;  
```  
  
## Return Value  
 Nonzero if the recordset contains no records or if you have scrolled beyond the last record; otherwise 0.  
  
## Remarks  
 Call this member function as you scroll from record to record to learn whether you have gone beyond the last record of the recordset. You can also use `IsEOF` to determine whether the recordset contains any records or is empty. Immediately after you call **Open**, if the recordset contains no records, `IsEOF` returns nonzero. When you open a recordset that has at least one record, the first record is the current record and `IsEOF` returns 0.  
  
 If the last record is the current record when you call `MoveNext`, `IsEOF` will subsequently return nonzero. If `IsEOF` returns nonzero and you call `MoveNext`, an error occurs. If `IsEOF` returns nonzero, the current record is undefined, and any action that requires a current record will result in an error.  
  
## Example  
 See the example for [IsBOF](../vs140/CRecordset--IsBOF.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::IsBOF](../vs140/CRecordset--IsBOF.md)   
 [CRecordset::MoveLast](../vs140/CRecordset--MoveLast.md)   
 [CRecordset::MoveNext](../vs140/CRecordset--MoveNext.md)