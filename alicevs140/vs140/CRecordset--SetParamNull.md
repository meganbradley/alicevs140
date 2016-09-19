---
title: "CRecordset::SetParamNull"
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
ms.assetid: d24a7cec-3fdf-4a7d-8cfb-571fc101e2ae
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::SetParamNull
Flags a parameter as Null (specifically having no value) or as non-Null.  
  
## Syntax  
  
```  
  
      void SetParamNull(  
   int nIndex,  
   BOOL bNull = TRUE   
);  
```  
  
#### Parameters  
 `nIndex`  
 The zero-based index of the parameter.  
  
 `bNull`  
 If **TRUE** (the default value), the parameter is flagged as Null. Otherwise, the parameter is flagged as non-Null.  
  
## Remarks  
 Unlike [SetFieldNull](../vs140/CRecordset--SetFieldNull.md), you can call `SetParamNull` before you have opened the recordset.  
  
 `SetParamNull` is typically used with predefined queries (stored procedures).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::FlushResultSet](../vs140/CRecordset--FlushResultSet.md)