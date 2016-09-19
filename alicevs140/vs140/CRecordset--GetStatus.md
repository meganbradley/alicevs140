---
title: "CRecordset::GetStatus"
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
ms.assetid: 9f8e2fb5-5d3c-4634-8f87-500f4a556f1f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::GetStatus
Determines the index of the current record in the recordset and whether the last record has been seen.  
  
## Syntax  
  
```  
  
      void GetStatus(  
   CRecordsetStatus& rStatus   
) const;  
```  
  
#### Parameters  
 `rStatus`  
 A reference to a **CRecordsetStatus** object. See the Remarks section for more information.  
  
## Remarks  
 `CRecordset` attempts to track the index, but under some circumstances this may not be possible. See [GetRecordCount](../vs140/CRecordset--GetRecordCount.md) for an explanation.  
  
 The **CRecordsetStatus** structure has the following form:  
  
 `struct CRecordsetStatus`  
  
 `{`  
  
 `long m_lCurrentRecord;`  
  
 `BOOL m_bRecordCountFinal;`  
  
 `};`  
  
 The two members of **CRecordsetStatus** have the following meanings:  
  
-   **m_lCurrentRecord** Contains the zero-based index of the current record in the recordset, if known. If the index cannot be determined, this member contains **AFX_CURRENT_RECORD_UNDEFINED** (–2). If `IsBOF` is **TRUE** (empty recordset or attempt to scroll before first record), then **m_lCurrentRecord** is set to **AFX_CURRENT_RECORD_BOF** (–1). If on the first record, then it is set to 0, second record 1, and so on.  
  
-   **m_bRecordCountFinal** Nonzero if the total number of records in the recordset has been determined. Generally this must be accomplished by starting at the beginning of the recordset and calling `MoveNext` until `IsEOF` returns nonzero. If this member is zero, the record count as returned by `GetRecordCount`, if not –1, is only a "high water mark" count of the records.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::GetRecordCount](../vs140/CRecordset--GetRecordCount.md)