---
title: "CRecordset::MoveNext"
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
ms.assetid: abb9512d-e08f-4621-8799-aa7b36530b70
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::MoveNext
Makes the first record in the next rowset the current record.  
  
## Syntax  
  
```  
  
void MoveNext( );  
  
```  
  
## Remarks  
 If you have not implemented bulk row fetching, your recordset has a rowset size of 1, so `MoveNext` simply moves to the next record.  
  
> [!NOTE]
>  When you move through a recordset, you cannot skip deleted records. See the [IsDeleted](../vs140/CRecordset--IsDeleted.md) member function for details.  
  
> [!CAUTION]
>  Calling any of the **Move** functions throws an exception if the recordset has no records. To determine whether the recordset has any records, call `IsBOF` and `IsEOF`.  
  
> [!NOTE]
>  It is also recommended that you call `IsEOF` before calling `MoveNext`. For example, if you have scrolled past the end of the recordset, `IsEOF` will return nonzero; a subsequent call to `MoveNext` would throw an exception.  
  
> [!NOTE]
>  If you call any of the **Move** functions while the current record is being updated or added, the updates are lost without warning.  
  
 For more information about recordset navigation, see the articles [Recordset: Scrolling (ODBC)](../vs140/Recordset--Scrolling--ODBC-.md) and [Recordset: Bookmarks and Absolute Positions (ODBC)](../vs140/Recordset--Bookmarks-and-Absolute-Positions--ODBC-.md). For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
## Exceptions  
 This method can throw exceptions of type **CDBException\*** and `CMemoryException*`.  
  
## Example  
 See the example for [IsBOF](../vs140/CRecordset--IsBOF.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::Move](../vs140/CRecordset--Move.md)   
 [CRecordset::MovePrev](../vs140/CRecordset--MovePrev.md)   
 [CRecordset::MoveFirst](../vs140/CRecordset--MoveFirst.md)   
 [CRecordset::MoveLast](../vs140/CRecordset--MoveLast.md)   
 [CRecordset::IsBOF](../vs140/CRecordset--IsBOF.md)   
 [CRecordset::IsEOF](../vs140/CRecordset--IsEOF.md)