---
title: "CRecordset::SetFieldNull"
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
ms.assetid: 471ede61-0f10-4ac5-9ac7-010e5be2f2c3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::SetFieldNull
Flags a field data member of the recordset as Null (specifically having no value) or as non-Null.  
  
## Syntax  
  
```  
  
      void SetFieldNull(  
   void* pv,  
   BOOL bNull = TRUE   
);  
```  
  
#### Parameters  
 `pv`  
 Contains the address of a field data member in the recordset or **NULL**. If **NULL**, all field data members in the recordset are flagged. (C++ **NULL** is not the same as Null in database terminology, which means "having no value.")  
  
 `bNull`  
 Nonzero if the field data member is to be flagged as having no value (Null). Otherwise 0 if the field data member is to be flagged as non-Null.  
  
## Remarks  
 When you add a new record to a recordset, all field data members are initially set to a Null value and flagged as "dirty" (changed). When you retrieve a record from a data source, its columns either already have values or are Null.  
  
> [!NOTE]
>  Do not call this member function on recordsets that are using bulk row fetching. If you have implemented bulk row fetching, calling `SetFieldNull` results in a failed assertion. For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
 If you specifically wish to designate a field of the current record as not having a value, call `SetFieldNull` with `bNull` set to **TRUE** to flag it as Null. If a field was previously marked Null and you now want to give it a value, simply set its new value. You do not have to remove the Null flag with `SetFieldNull`. To determine whether the field is allowed to be Null, call `IsFieldNullable`.  
  
> [!CAUTION]
>  Call this member function only after you have called [Edit](../vs140/CRecordset--Edit.md) or [AddNew](../vs140/CRecordset--AddNew.md).  
  
 Using **NULL** for the first argument of the function will apply the function only to **outputColumn** fields, not **param** fields. For instance, the call  
  
 [!CODE [NVC_MFCDatabase#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#26)]  
  
 will set only **outputColumn** fields to **NULL**; **param** fields will be unaffected.  
  
 To work on **param** fields, you must supply the actual address of the individual **param** you want to work on, such as:  
  
 [!CODE [NVC_MFCDatabase#27](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#27)]  
  
 This means you cannot set all **param** fields to **NULL**, as you can with **outputColumn** fields.  
  
> [!NOTE]
>  When setting parameters to Null, a call to `SetFieldNull` before the recordset is opened results in an assertion. In this case, call [SetParamNull](../vs140/CRecordset--SetParamNull.md).  
  
 `SetFieldNull` is implemented through [DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::IsFieldNull](../vs140/CRecordset--IsFieldNull.md)   
 [CRecordset::SetFieldDirty](../vs140/CRecordset--SetFieldDirty.md)   
 [CRecordset::Edit](../vs140/CRecordset--Edit.md)   
 [CRecordset::Update](../vs140/CRecordset--Update.md)   
 [CRecordset::IsFieldNullable](../vs140/CRecordset--IsFieldNullable.md)