---
title: "RFX_Binary"
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
ms.assetid: 908ff945-3ad0-43a1-9932-cdcdc8b14915
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RFX_Binary
Transfers arrays of bytes between the field data members of a `CRecordset` object and the columns of a record on the data source of ODBC type **SQL_BINARY**, **SQL_VARBINARY**, or **SQL_LONGVARBINARY**.  
  
## Syntax  
  
```  
  
      void RFX_Binary(  
   CFieldExchange* pFX,  
   const char* szName,  
   CByteArray& value,  
   int nMaxLength = 255   
);  
```  
  
#### Parameters  
 `pFX`  
 A pointer to an object of class [CFieldExchange](../vs140/CFieldExchange-Class.md). This object contains information to define the context for each call of the function. For more information about the operations a `CFieldExchange` object can specify, see the article [Record Field Exchange: How RFX Works](../vs140/Record-Field-Exchange--How-RFX-Works.md).  
  
 `szName`  
 The name of a data column.  
  
 *value*  
 The value stored in the indicated data member — the value to be transferred. For a transfer from recordset to data source, the value, of type [CByteArray](../vs140/CByteArray-Class.md), is taken from the specified data member. For a transfer from data source to recordset, the value is stored in the specified data member.  
  
 `nMaxLength`  
 The maximum allowed length of the string or array being transferred. The default value of `nMaxLength` is 255. Legal values are 1 to [INT_MAX](../vs140/Data-Type-Constants.md). The framework allocates this amount of space for the data. For best performance, pass a value large enough to accommodate the largest data item you expect.  
  
## Remarks  
 Data in the data source of these types is mapped to and from type `CByteArray` in the recordset.  
  
## Example  
 See [RFX_Text](../vs140/RFX_Text.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [RFX_Text](../vs140/RFX_Text.md)   
 [RFX_Bool](../vs140/RFX_Bool.md)   
 [RFX_Long](../vs140/RFX_Long.md)   
 [RFX_Int](../vs140/RFX_Int.md)   
 [RFX_Single](../vs140/RFX_Single.md)   
 [RFX_Double](../vs140/RFX_Double.md)   
 [RFX_Date](../vs140/RFX_Date.md)   
 [RFX_Byte](../vs140/RFX_Byte.md)   
 [RFX_LongBinary](../vs140/RFX_LongBinary.md)   
 [CFieldExchange::SetFieldType](../vs140/CFieldExchange--SetFieldType.md)