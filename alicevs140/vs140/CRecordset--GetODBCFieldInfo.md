---
title: "CRecordset::GetODBCFieldInfo"
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
ms.assetid: 83193643-ef89-403e-86db-318b97822762
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::GetODBCFieldInfo
Obtains information about the fields in the recordset.  
  
## Syntax  
  
```  
  
      void GetODBCFieldInfo(   
   LPCTSTR lpszName,   
   CODBCFieldInfo& fieldinfo    
);  
void GetODBCFieldInfo(   
   short nIndex,   
   CODBCFieldInfo& fieldinfo    
);  
```  
  
#### Parameters  
 `lpszName`  
 The name of a field.  
  
 `fieldinfo`  
 A reference to a `CODBCFieldInfo` structure.  
  
 `nIndex`  
 The zero-based index of the field.  
  
## Remarks  
 One version of the function lets you look up a field by name. The other version lets you look up a field by index.  
  
 For a description about the information returned, see the [CODBCFieldInfo](../vs140/CODBCFieldInfo-Structure.md) structure.  
  
 For more information about creating recordsets, see the article [Recordset: Creating and Closing Recordsets (ODBC)](../vs140/Recordset--Creating-and-Closing-Recordsets--ODBC-.md).  
  
## Exceptions  
 This method can throw exceptions of type **CDBException\***.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::GetFieldValue](../vs140/CRecordset--GetFieldValue.md)   
 [CODBCFieldInfo Structure](../vs140/CODBCFieldInfo-Structure.md)