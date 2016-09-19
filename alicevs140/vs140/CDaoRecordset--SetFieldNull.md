---
title: "CDaoRecordset::SetFieldNull"
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
ms.assetid: ba3674c6-f436-4c60-a976-727b45199a55
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::SetFieldNull
Call this member function to flag a field data member of the recordset as Null (specifically having no value) or as non-Null.  
  
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
 `SetFieldNull` is used for fields bound in the `DoFieldExchange` mechanism.  
  
 When you add a new record to a recordset, all field data members are initially set to a Null value and flagged as "dirty" (changed). When you retrieve a record from a data source, its columns either already have values or are Null. If it is not appropriate to make a field Null, a [CDaoException](../vs140/CDaoException-Class.md) is thrown.  
  
 If you are using the double-buffering mechanism, for example, if you specifically wish to designate a field of the current record as not having a value, call `SetFieldNull` with `bNull` set to **TRUE** to flag it as Null. If a field was previously marked Null and you now want to give it a value, simply set its new value. You do not have to remove the Null flag with `SetFieldNull`. To determine whether the field is allowed to be Null, call [IsFieldNullable](../vs140/CDaoRecordset--IsFieldNullable.md).  
  
 If you are not using the double-buffering mechanism, then changing the value of the field does not automatically set the field as dirty and non-Null. You must specifically set the fields dirty and non-Null. The flag contained in [m_bCheckCacheForDirtyFields](../vs140/CDaoRecordset--m_bCheckCacheForDirtyFields.md) controls this automatic field checking.  
  
 The DFX mechanism employs the use of **PSEUDO NULL**. For more information, see [CDaoFieldExchange::m_nOperation](../vs140/CDaoFieldExchange--m_nOperation.md).  
  
> [!NOTE]
>  Call this member function only after you have called [Edit](../vs140/CDaoRecordset--Edit.md) or [AddNew](../vs140/CDaoRecordset--AddNew.md).  
  
 Using **NULL** for the first argument of the function will apply the function only to **outputColumn** fields, not **param** fields in `CDaoFieldExchange`. For instance, the call  
  
 [!CODE [NVC_MFCDatabase#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#8)]  
  
 will set only **outputColumn** fields to **NULL**; **param** fields will be unaffected.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::SetParamValue](../vs140/CDaoRecordset--SetParamValue.md)