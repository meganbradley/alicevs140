---
title: "CDaoFieldExchange::m_nOperation"
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
ms.assetid: 7dec3198-00ad-4e26-9bd5-ac8ba5c8a90c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoFieldExchange::m_nOperation
Identifies the operation to be performed on the [CDaoRecordset](../vs140/CDaoRecordset-Class.md) object associated with the field exchange object.  
  
## Remarks  
 The `CDaoFieldExchange` object supplies the context for a number of different DFX operations on the recordset.  
  
> [!NOTE]
>  The **PSEUDO NULL** value described under the MarkForAddNew and SetFieldNull operations below is a value used to mark fields Null. The DAO record field exchange mechanism (DFX) uses this value to determine which fields have been explicitly marked Null. **PSEUDO NULL** is not required for [COleDateTime](../vs140/COleDateTime-Class.md) and [COleCurrency](../vs140/COleCurrency-Class.md) fields.  
  
 Possible values of **m_nOperation** are:  
  
|Operation|Description|  
|---------------|-----------------|  
|**AddToParameterList**|Builds the **PARAMETERS** clause of the SQL statement.|  
|**AddToSelectList**|Builds the **SELECT** clause of the SQL statement.|  
|**BindField**|Binds a field in the database to a memory location in your application.|  
|**BindParam**|Sets parameter values for the recordset's query.|  
|**Fixup**|Sets the Null status for a field.|  
|**AllocCache**|Allocates the cache used to check for "dirty" fields in the recordset.|  
|**StoreField**|Saves the current record to the cache.|  
|**LoadField**|Restores the cached data member variables in the recordset.|  
|**FreeCache**|Frees the cache used to check for "dirty" fields in the recordset.|  
|`SetFieldNull`|Sets a field's status to Null and value to **PSEUDO NULL**.|  
|**MarkForAddNew**|Marks fields "dirty" if not **PSEUDO NULL**.|  
|**MarkForEdit**|Marks fields "dirty" if they do not match the cache.|  
|**SetDirtyField**|Sets field values marked as "dirty."|  
|**DumpField**|Dumps a field's contents (debug only).|  
|**MaxDFXOperation**|Used for input checking.|  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoFieldExchange Class](../vs140/CDaoFieldExchange-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoFieldExchange::IsValidOperation](../vs140/CDaoFieldExchange--IsValidOperation.md)   
 [CDaoFieldExchange::m_prs](../vs140/CDaoFieldExchange--m_prs.md)   
 [CDaoRecordset::DoFieldExchange](../vs140/CDaoRecordset--DoFieldExchange.md)