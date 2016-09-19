---
title: "CRecordset::GetFieldValue"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 7baf0a0c-2ef3-4ed8-8377-95bff3599788
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::GetFieldValue
Retrieves field data in the current record.  
  
## Syntax  
  
```  
  
      void GetFieldValue(   
   LPCTSTR lpszName,   
   CDBVariant& varValue,   
   short nFieldType = DEFAULT_FIELD_TYPE    
);  
void GetFieldValue(   
   short nIndex,   
   CDBVariant& varValue,   
   short nFieldType = DEFAULT_FIELD_TYPE    
);  
void GetFieldValue(  
   short nIndex,  
   CStringA& strValue   
);  
void GetFieldValue(  
   short nIndex,  
   CStringW& strValue   
);  
```  
  
#### Parameters  
 `lpszName`  
 The name of a field.  
  
 *varValu*e  
 A reference to a [CDBVariant](../vs140/CDBVariant-Class.md) object that will store the field's value.  
  
 `nFieldType`  
 The ODBC C data type of the field. Using the default value, **DEFAULT_FIELD_TYPE**, forces `GetFieldValue` to determine the C data type from the SQL data type, based on the following table. Otherwise, you can specify the data type directly or choose a compatible data type; for example, you can store any data type into **SQL_C_CHAR**.  
  
|C data type|SQL data type|  
|-----------------|-------------------|  
|**SQL_C_BIT**|**SQL_BIT**|  
|**SQL_C_UTINYINT**|**SQL_TINYINT**|  
|**SQL_C_SSHORT**|**SQL_SMALLINT**|  
|**SQL_C_SLONG**|**SQL_INTEGER**|  
|**SQL_C_FLOAT**|**SQL_REAL**|  
|**SQL_C_DOUBLE**|**SQL_FLOATSQL_DOUBLE**|  
|**SQL_C_TIMESTAMP**|**SQL_DATESQL_TIMESQL_TIMESTAMP**|  
|**SQL_C_CHAR**|**SQL_NUMERICSQL_DECIMALSQL_BIGINTSQL_CHARSQL_VARCHARSQL_LONGVARCHAR**|  
|**SQL_C_BINARY**|**SQL_BINARYSQL_VARBINARYSQL_LONGVARBINARY**|  
  
 For more information about ODBC data types, see the topics "SQL Data Types" and "C Data Types" in Appendix D of the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `nIndex`  
 The zero-based index of the field.  
  
 `strValue`  
 A reference to a [CString](../vs140/CStringT-Class.md) object that will store the field's value converted to text, regardless of the field's data type.  
  
## Remarks  
 You can look up a field either by name or by index. You can store the field value in either a `CDBVariant` object or a `CString` object.  
  
 If you have implemented bulk row fetching, the current record is always positioned on the first record in a rowset. To use `GetFieldValue` on a record within a given rowset, you must first call the [SetRowsetCursorPosition](../vs140/CRecordset--SetRowsetCursorPosition.md) member function to move the cursor to the desired row within that rowset. Then call `GetFieldValue` for that row. To implement bulk row fetching, you must specify the `CRecordset::useMultiRowFetch` option of the `dwOptions` parameter in the [Open](../vs140/CRecordset--Open.md) member function.  
  
 You can use `GetFieldValue` to dynamically fetch fields at run time rather than statically binding them at design time. For example, if you have declared a recordset object directly from `CRecordset`, you must use `GetFieldValue` to retrieve the field data; record field exchange (RFX), or bulk record field exchange (Bulk RFX), is not implemented.  
  
> [!NOTE]
>  If you declare a recordset object without deriving from `CRecordset`, do not have the ODBC Cursor Library loaded. The cursor library requires that the recordset have at least one bound column; however, when you use `CRecordset` directly, none of the columns are bound. The member functions [CDatabase::OpenEx](../vs140/CDatabase--OpenEx.md) and [CDatabase::Open](../vs140/CDatabase--Open.md) control whether the cursor library will be loaded.  
  
 `GetFieldValue` calls the ODBC API function **SQLGetData**. If your driver outputs the value **SQL_NO_TOTAL** for the actual length of the field value, `GetFieldValue` throws an exception. For more information about **SQLGetData**, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Exceptions  
 This method can throw exceptions of type **CDBException\*** and `CMemoryException*`.  
  
## Example  
 The following sample code illustrates calls to `GetFieldValue` for a recordset object declared directly from `CRecordset`.  
  
 [!CODE [NVC_MFCDatabase#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#23)]  
  
> [!NOTE]
>  Unlike the DAO class `CDaoRecordset`, `CRecordset` does not have a `SetFieldValue` member function. If you create an object directly from `CRecordset`, it is effectively read-only.  
  
 For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md)   
 [CRecordset::DoBulkFieldExchange](../vs140/CRecordset--DoBulkFieldExchange.md)   
 [CRecordset::GetODBCFieldCount](../vs140/CRecordset--GetODBCFieldCount.md)   
 [CRecordset::GetODBCFieldInfo](../vs140/CRecordset--GetODBCFieldInfo.md)   
 [CRecordset::SetRowsetCursorPosition](../vs140/CRecordset--SetRowsetCursorPosition.md)