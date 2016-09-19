---
title: "CODBCFieldInfo Structure"
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
ms.topic: article
ms.assetid: 92598b4f-facc-4108-b282-63a179ff79ab
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CODBCFieldInfo Structure
The `CODBCFieldInfo` structure contains information about the fields in an ODBC data source.  
  
## Syntax  
  
```  
  
      struct CODBCFieldInfo  
{  
   CString m_strName;  
   SWORD m_nSQLType;  
   UDWORD m_nPrecision;  
   SWORD m_nScale;  
   SWORD m_nNullability;  
};  
```  
  
#### Parameters  
 `m_strName`  
 The name of the field.  
  
 *m_nSQLType*  
 The SQL data type of the field. This can be an ODBC SQL data type or a driver-specific SQL data type. For a list of valid ODBC SQL data types, see "SQL Data Types" in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For information about driver-specific SQL data types, see the driver's documentation.  
  
 *m_nPrecision*  
 The maximum precision of the field. For details, see "Precision, Scale, Length, and Display Size" in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 *m_nScale*  
 The scale of the field. For details, see "Precision, Scale, Length, and Display Size" in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 *m_nNullability*  
 Whether the field accepts a Null value. This can be one of two values: **SQL_NULLABLE** if the field accepts Null values, or **SQL_NO_NULLS** if the field does not accept Null values.  
  
## Remarks  
 To retrieve this information, call [CRecordset::GetODBCFieldInfo](../vs140/CRecordset--GetODBCFieldInfo.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [Structures, Styles, Callbacks, and Message Maps](../vs140/Structures--Styles--Callbacks--and-Message-Maps.md)   
 [CRecordset::GetODBCFieldInfo](../vs140/CRecordset--GetODBCFieldInfo.md)   
 [CRecordset::GetFieldValue](../vs140/CRecordset--GetFieldValue.md)