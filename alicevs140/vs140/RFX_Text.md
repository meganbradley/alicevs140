---
title: "RFX_Text"
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
ms.assetid: de3c7581-d26c-40cb-81f3-c492ef4809f6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RFX_Text
Transfers `CString` data between the field data members of a `CRecordset` object and columns of a record on the data source of ODBC type **SQL_LONGVARCHAR**, **SQL_CHAR**, **SQL_VARCHAR**, **SQL_DECIMAL**, or **SQL_NUMERIC**.  
  
## Syntax  
  
```  
  
      void RFX_Text(  
   CFieldExchange* pFX,  
   const char* szName,  
   CString& value,  
   int nMaxLength = 255,  
   int nColumnType = SQL_VARCHAR,  
   short nScale = 0   
);  
```  
  
#### Parameters  
 `pFX`  
 A pointer to an object of class `CFieldExchange`. This object contains information to define the context for each call of the function. For more information about the operations a `CFieldExchange` object can specify, see the article [Record Field Exchange: How RFX Works](../vs140/Record-Field-Exchange--How-RFX-Works.md).  
  
 `szName`  
 The name of a data column.  
  
 *value*  
 The value stored in the indicated data member — the value to be transferred. For a transfer from recordset to data source, the value, of type `CString`, is taken from the specified data member. For a transfer from data source to recordset, the value is stored in the specified data member.  
  
 `nMaxLength`  
 The maximum allowed length of the string or array being transferred. The default value of `nMaxLength` is 255. Legal values are 1 to [INT_MAX](../vs140/Data-Type-Constants.md). The framework allocates this amount of space for the data. For best performance, pass a value large enough to accommodate the largest data item you expect.  
  
 *nColumnType*  
 Used mainly for parameters. An integer indicating the data type of the parameter. The type is an ODBC data type of the form **SQL_XXX**.  
  
 `nScale`  
 Specifies the scale for values of ODBC type **SQL_DECIMAL** or **SQL_NUMERIC**. `nScale` is only useful when setting parameter values. For more information, see the topic "Precision, Scale, Length, and Display Size" in Appendix D of the *ODBC SDK Programmer's Reference*.  
  
## Remarks  
 Data in the data source of all of these types is mapped to and from `CString` in the recordset.  
  
## Example  
 This example shows several calls to `RFX_Text`. Notice also the two calls to `CFieldExchange::SetFieldType`. For parameters you must write the call to `SetFieldType` and its RFX call. The output column call and its associated RFX calls are normally written by a code wizard.  
  
 [!CODE [NVC_MFCDatabase#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#19)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [RFX_Bool](../vs140/RFX_Bool.md)   
 [RFX_Long](../vs140/RFX_Long.md)   
 [RFX_Int](../vs140/RFX_Int.md)   
 [RFX_Single](../vs140/RFX_Single.md)   
 [RFX_Double](../vs140/RFX_Double.md)   
 [RFX_Date](../vs140/RFX_Date.md)   
 [RFX_Byte](../vs140/RFX_Byte.md)   
 [RFX_Binary](../vs140/RFX_Binary.md)   
 [RFX_LongBinary](../vs140/RFX_LongBinary.md)   
 [CFieldExchange::SetFieldType](../vs140/CFieldExchange--SetFieldType.md)