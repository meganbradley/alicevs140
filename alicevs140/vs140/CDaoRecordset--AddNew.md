---
title: "CDaoRecordset::AddNew"
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
ms.assetid: af878273-0094-4c9e-911d-5aa7cd243a14
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::AddNew
Call this member function to add a new record to a table-type or dynaset-type recordset.  
  
## Syntax  
  
```  
  
virtual void AddNew( );  
  
```  
  
## Remarks  
 The record's fields are initially Null. (In database terminology, Null means "having no value" and is not the same as **NULL** in C++.) To complete the operation, you must call the [Update](../vs140/CDaoRecordset--Update.md) member function. **Update** saves your changes to the data source.  
  
> [!CAUTION]
>  If you edit a record and then scroll to another record without calling **Update**, your changes are lost without warning.  
  
 If you add a record to a dynaset-type recordset by calling [AddNew](#_mfc_cdaorecordset.3a3a.addnew), the record is visible in the recordset and included in the underlying table where it becomes visible to any new `CDaoRecordset` objects.  
  
 The position of the new record depends on the type of recordset:  
  
-   In a dynaset-type recordset, where the new record is inserted is not guaranteed. This behavior changed with Microsoft Jet 3.0 for reasons of performance and concurrency. If your goal is to make the newly added record the current record, get the bookmark of the last modified record and move to that bookmark:  
  
     [!CODE [NVC_MFCDatabase#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#1)]  
  
-   In a table-type recordset for which an index has been specified, records are returned in their proper place in the sort order. If no index has been specified, new records are returned at the end of the recordset.  
  
 The record that was current before you used `AddNew` remains current. If you want to make the new record current and the recordset supports bookmarks, call [SetBookmark](../vs140/CDaoRecordset--SetBookmark.md) to the bookmark identified by the LastModified property setting of the underlying DAO recordset object. Doing so is useful for determining the value for counter (auto-increment) fields in an added record. For more information, see [GetLastModifiedBookmark](../vs140/CDaoRecordset--GetLastModifiedBookmark.md).  
  
 If the database supports transactions, you can make your `AddNew` call part of a transaction. For more information about transactions, see class [CDaoWorkspace](../vs140/CDaoWorkspace-Class.md). Note that you should call [CDaoWorkspace::BeginTrans](../vs140/CDaoWorkspace--BeginTrans.md) before calling `AddNew`.  
  
 It is illegal to call `AddNew` for a recordset whose [Open](../vs140/CDaoRecordset--Open.md) member function has not been called. A `CDaoException` is thrown if you call `AddNew` for a recordset that cannot be appended. You can determine whether the recordset is updateable by calling [CanAppend](../vs140/CDaoRecordset--CanAppend.md).  
  
 The framework marks changed field data members to ensure they will be written to the record on the data source by the DAO record field exchange (DFX) mechanism. Changing the value of a field generally sets the field dirty automatically, so you will seldom need to call [SetFieldDirty](../vs140/CDaoRecordset--SetFieldDirty.md) yourself, but you might sometimes want to ensure that columns will be explicitly updated or inserted regardless of what value is in the field data member. The DFX mechanism also employs the use of **PSEUDO NULL**. For more information, see [CDaoFieldExchange::m_nOperation](../vs140/CDaoFieldExchange--m_nOperation.md).  
  
 If the double-buffering mechanism is not being used, then changing the value of the field does not automatically set the field as dirty. In this case, it will be necessary to explicitly set the field dirty. The flag contained in [m_bCheckCacheForDirtyFields](../vs140/CDaoRecordset--m_bCheckCacheForDirtyFields.md) controls this automatic field checking.  
  
> [!NOTE]
>  If records are double-buffered (that is, automatic field checking is enabled), calling `CancelUpdate` will restore the member variables to the values they had before `AddNew` or **Edit** was called.  
  
 For related information, see the topics "AddNew Method", "CancelUpdate Method", "LastModified Property", and "EditMode Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::CanUpdate](../vs140/CDaoRecordset--CanUpdate.md)   
 [CDaoRecordset::CancelUpdate](../vs140/CDaoRecordset--CancelUpdate.md)   
 [CDaoRecordset::Delete](../vs140/CDaoRecordset--Delete.md)   
 [CDaoRecordset::Edit](../vs140/CDaoRecordset--Edit.md)   
 [CDaoRecordset::Update](../vs140/CDaoRecordset--Update.md)   
 [CDaoRecordset::CanTransact](../vs140/CDaoRecordset--CanTransact.md)