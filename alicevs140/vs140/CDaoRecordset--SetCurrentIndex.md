---
title: "CDaoRecordset::SetCurrentIndex"
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
ms.assetid: 74c909a2-c2fe-4cd5-8af9-b7513b9f75db
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::SetCurrentIndex
Call this member function to set an index on a table-type recordset.  
  
## Syntax  
  
```  
  
      void SetCurrentIndex(  
   LPCTSTR lpszIndex   
);  
```  
  
#### Parameters  
 `lpszIndex`  
 A pointer containing the name of the index to be set.  
  
## Remarks  
 Records in base tables are not stored in any particular order. Setting an index changes the order of records returned from the database, but it does not affect the order in which the records are stored. The specified index must already be defined. If you try to use an index object that does not exist, or if the index is not set when you call [Seek](../vs140/CDaoRecordset--Seek.md), MFC throws an exception.  
  
 You can create a new index for the table by calling [CDaoTableDef::CreateIndex](../vs140/CDaoTableDef--CreateIndex.md) and appending the new index to the Indexes collection of the underlying tabledef by calling [CDaoTableDef::Append](../vs140/CDaoTableDef--Append.md), and then reopening the recordset.  
  
 Records returned from a table-type recordset can be ordered only by the indexes defined for the underlying tabledef. To sort records in some other order, you can open a dynaset-type or snapshot-type recordset using a SQL **ORDER BY** clause stored in [CDaoRecordset::m_strSort](../vs140/CDaoRecordset--m_strSort.md).  
  
 For related information, see the topic "Index Object" and the definition "current index" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetCurrentIndex](../vs140/CDaoRecordset--GetCurrentIndex.md)