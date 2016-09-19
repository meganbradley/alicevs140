---
title: "CRecordset::IsFieldDirty"
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
ms.assetid: eada4a36-aceb-4932-80a2-eade7eadb981
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::IsFieldDirty
Determines whether the specified field data member has been changed since [Edit](../vs140/CRecordset--Edit.md) or [AddNew](../vs140/CRecordset--AddNew.md) was called.  
  
## Syntax  
  
```  
  
      BOOL IsFieldDirty(   
   void * pv    
);  
```  
  
#### Parameters  
 `pv`  
 A pointer to the field data member whose status you want to check, or **NULL** to determine if any of the fields are dirty.  
  
## Return Value  
 Nonzero if the specified field data member has changed since calling `AddNew` or **Edit**; otherwise 0.  
  
## Remarks  
 The data in all dirty field data members will be transferred to the record on the data source when the current record is updated by a call to the [Update](../vs140/CRecordset--Update.md) member function of `CRecordset` (following a call to **Edit** or `AddNew`).  
  
> [!NOTE]
>  This member function is not applicable on recordsets that are using bulk row fetching. If you have implemented bulk row fetching, then `IsFieldDirty` will always return **FALSE** and will result in a failed assertion. For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
 Calling `IsFieldDirty` will reset the effects of preceding calls to [SetFieldDirty](../vs140/CRecordset--SetFieldDirty.md) since the dirty status of the field is re-evaluated. In the `AddNew` case, if the current field value differs from the pseudo null value, the field status is set dirty. In the **Edit** case, if the field value differs from the cached value, then the field status is set dirty.  
  
 `IsFieldDirty` is implemented through [DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md).  
  
 For more information on the dirty flag, see the article [Recordset: How Recordsets Select Records (ODBC)](../vs140/Recordset--How-Recordsets-Select-Records--ODBC-.md).  
  
## Exceptions  
 This method can throw exceptions of type `CMemoryException*`.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::SetFieldDirty](../vs140/CRecordset--SetFieldDirty.md)   
 [CRecordset::IsFieldNull](../vs140/CRecordset--IsFieldNull.md)