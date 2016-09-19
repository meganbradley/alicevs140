---
title: "CRecordset::SetFieldDirty"
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
ms.assetid: d58037cb-e0bc-4dec-8892-ff73f4c9dbd7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::SetFieldDirty
Flags a field data member of the recordset as changed or as unchanged.  
  
## Syntax  
  
```  
  
      void SetFieldDirty(  
   void* pv,  
   BOOL bDirty = TRUE   
);  
```  
  
#### Parameters  
 `pv`  
 Contains the address of a field data member in the recordset or **NULL**. If **NULL**, all field data members in the recordset are flagged. (C++ **NULL** is not the same as Null in database terminology, which means "having no value.")  
  
 `bDirty`  
 **TRUE** if the field data member is to be flagged as "dirty" (changed). Otherwise **FALSE** if the field data member is to be flagged as "clean" (unchanged).  
  
## Remarks  
 Marking fields as unchanged ensures the field is not updated and results in less SQL traffic.  
  
> [!NOTE]
>  This member function is not applicable on recordsets that are using bulk row fetching. If you have implemented bulk row fetching, then `SetFieldDirty` will result in a failed assertion. For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
 The framework marks changed field data members to ensure they will be written to the record on the data source by the record field exchange (RFX) mechanism. Changing the value of a field generally sets the field dirty automatically, so you will seldom need to call `SetFieldDirty` yourself, but you might sometimes want to ensure that columns will be explicitly updated or inserted regardless of what value is in the field data member.  
  
> [!CAUTION]
>  Call this member function only after you have called [Edit](../vs140/CRecordset--Edit.md) or [AddNew](../vs140/CRecordset--AddNew.md).  
  
 Using **NULL** for the first argument of the function will apply the function only to **outputColumn** fields, not **param** fields. For instance, the call  
  
 [!CODE [NVC_MFCDatabase#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#26)]  
  
 will set only **outputColumn** fields to **NULL**; **param** fields will be unaffected.  
  
 To work on **param** fields, you must supply the actual address of the individual **param** you want to work on, such as:  
  
 [!CODE [NVC_MFCDatabase#27](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#27)]  
  
 This means you cannot set all **param** fields to **NULL**, as you can with **outputColumn** fields.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::IsFieldDirty](../vs140/CRecordset--IsFieldDirty.md)   
 [CRecordset::SetFieldNull](../vs140/CRecordset--SetFieldNull.md)   
 [CRecordset::Edit](../vs140/CRecordset--Edit.md)   
 [CRecordset::Update](../vs140/CRecordset--Update.md)