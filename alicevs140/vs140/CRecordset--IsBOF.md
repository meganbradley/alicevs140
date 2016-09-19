---
title: "CRecordset::IsBOF"
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
ms.assetid: db4dcc52-54fd-4d6f-99d1-183d3741fff4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::IsBOF
Returns nonzero if the recordset has been positioned before the first record. There is no current record.  
  
## Syntax  
  
```  
  
BOOL IsBOF( ) const;  
```  
  
## Return Value  
 Nonzero if the recordset contains no records or if you have scrolled backward before the first record; otherwise 0.  
  
## Remarks  
 Call this member function before you scroll from record to record to learn whether you have gone before the first record of the recordset. You can also use `IsBOF` along with `IsEOF` to determine whether the recordset contains any records or is empty. Immediately after you call **Open**, if the recordset contains no records, `IsBOF` returns nonzero.When you open a recordset that has at least one record, the first record is the current record and `IsBOF` returns 0.  
  
 If the first record is the current record and you call `MovePrev`, `IsBOF` will subsequently return nonzero. If `IsBOF` returns nonzero and you call `MovePrev`, an error occurs. If `IsBOF` returns nonzero, the current record is undefined, and any action that requires a current record will result in an error.  
  
## Example  
 This example uses `IsBOF` and `IsEOF` to detect the limits of a recordset as the code scrolls through the recordset in both directions.  
  
 [!CODE [NVC_MFCDatabase#25](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#25)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::IsEOF](../vs140/CRecordset--IsEOF.md)   
 [CRecordset::MoveFirst](../vs140/CRecordset--MoveFirst.md)   
 [CRecordset::MovePrev](../vs140/CRecordset--MovePrev.md)