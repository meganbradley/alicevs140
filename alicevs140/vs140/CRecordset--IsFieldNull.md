---
title: "CRecordset::IsFieldNull"
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
ms.assetid: 4409d56b-5870-4b37-adb4-d8d6d4732f0a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::IsFieldNull
Returns nonzero if the specified field in the current record is Null (has no value).  
  
## Syntax  
  
```  
  
      BOOL IsFieldNull(   
   void * pv    
);  
```  
  
#### Parameters  
 `pv`  
 A pointer to the field data member whose status you want to check, or **NULL** to determine if any of the fields are Null.  
  
## Return Value  
 Nonzero if the specified field data member is flagged as Null; otherwise 0.  
  
## Remarks  
 Call this member function to determine whether the specified field data member of a recordset has been flagged as Null. (In database terminology, Null means "having no value" and is not the same as **NULL** in C++.) If a field data member is flagged as Null, it is interpreted as a column of the current record for which there is no value.  
  
> [!NOTE]
>  This member function is not applicable on recordsets that are using bulk row fetching. If you have implemented bulk row fetching, then `IsFieldNull` will always return **FALSE** and will result in a failed assertion. For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
 `IsFieldNull` is implemented through [DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md).  
  
## Exceptions  
 This method can throw exceptions of type `CMemoryException*`.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::SetFieldNull](../vs140/CRecordset--SetFieldNull.md)   
 [CRecordset::IsFieldDirty](../vs140/CRecordset--IsFieldDirty.md)