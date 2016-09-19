---
title: "CRecordset::Requery"
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
ms.assetid: b9428878-1f85-4b0f-b897-8d9cdc6b7c3a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::Requery
Rebuilds (refreshes) a recordset.  
  
## Syntax  
  
```  
  
virtual BOOL Requery( );  
  
```  
  
## Return Value  
 Nonzero if the recordset was successfully rebuilt; otherwise 0.  
  
## Remarks  
 If any records are returned, the first record becomes the current record.  
  
 In order for the recordset to reflect the additions and deletions that you or other users are making to the data source, you must rebuild the recordset by calling **Requery**. If the recordset is a dynaset, it automatically reflects updates that you or other users make to its existing records (but not additions). If the recordset is a snapshot, you must call **Requery** to reflect edits by other users as well as additions and deletions.  
  
 For either a dynaset or a snapshot, call **Requery** any time you want to rebuild the recordset using a new filter or sort, or new parameter values. Set the new filter or sort property by assigning new values to **m_strFilter** and `m_strSort` before calling **Requery**. Set new parameters by assigning new values to parameter data members before calling **Requery**. If the filter and sort strings are unchanged, you can reuse the query, which improves performance.  
  
 If the attempt to rebuild the recordset fails, the recordset is closed. Before you call **Requery**, you can determine whether the recordset can be requeried by calling the `CanRestart` member function. `CanRestart` does not guarantee that **Requery** will succeed.  
  
> [!CAUTION]
>  Call **Requery** only after you have called [Open](../vs140/CRecordset--Open.md).  
  
## Exceptions  
 This method can throw exceptions of type **CDBException\*** and `CMemoryException*`.  
  
## Example  
 This example rebuilds a recordset to apply a different sort order.  
  
 [!CODE [NVC_MFCDatabase#29](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#29)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::CanRestart](../vs140/CRecordset--CanRestart.md)   
 [CRecordset::m_strFilter](../vs140/CRecordset--m_strFilter.md)   
 [CRecordset::m_strSort](../vs140/CRecordset--m_strSort.md)