---
title: "CDaoRecordset::SetFieldDirty"
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
ms.assetid: f37ab4d9-6501-450b-8c74-b9cc7bf47569
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::SetFieldDirty
Call this member function to flag a field data member of the recordset as changed or as unchanged.  
  
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
 Marking fields as unchanged ensures the field is not updated.  
  
 The framework marks changed field data members to ensure they will be written to the record on the data source by the DAO record field exchange (DFX) mechanism. Changing the value of a field generally sets the field dirty automatically, so you will seldom need to call `SetFieldDirty` yourself, but you might sometimes want to ensure that columns will be explicitly updated or inserted regardless of what value is in the field data member. The DFX mechanism also employs the use of **PSEUDO NULL**. For more information, see [CDaoFieldExchange::m_nOperation](../vs140/CDaoFieldExchange--m_nOperation.md).  
  
 If the double-buffering mechanism is not being used, then changing the value of the field does not automatically set the field as dirty. In this case, it will be necessary to explicitly set the field as dirty. The flag contained in [m_bCheckCacheForDirtyFields](../vs140/CDaoRecordset--m_bCheckCacheForDirtyFields.md) controls this automatic field checking.  
  
> [!NOTE]
>  Call this member function only after you have called [Edit](../vs140/CDaoRecordset--Edit.md) or [AddNew](../vs140/CDaoRecordset--AddNew.md).  
  
 Using **NULL** for the first argument of the function will apply the function to all **outputColumn** fields, not **param** fields in `CDaoFieldExchange`. For instance, the call  
  
 [!CODE [NVC_MFCDatabase#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#6)]  
  
 will set only **outputColumn** fields to **NULL**; **param** fields will be unaffected.  
  
 To work on a **param**, you must supply the actual address of the individual **param** you want to work on, such as:  
  
 [!CODE [NVC_MFCDatabase#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#7)]  
  
 This means you cannot set all **param** fields to **NULL**, as you can with **outputColumn** fields.  
  
 `SetFieldDirty` is implemented through `DoFieldExchange`.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::SetFieldNull](../vs140/CDaoRecordset--SetFieldNull.md)   
 [CDaoRecordset::SetFieldValue](../vs140/CDaoRecordset--SetFieldValue.md)