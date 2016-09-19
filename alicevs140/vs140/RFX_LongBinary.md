---
title: "RFX_LongBinary"
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
ms.assetid: 2249ff6d-1598-4660-9197-1fa1e4fc1451
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RFX_LongBinary
Transfers binary large object (BLOB) data using class [CLongBinary](../vs140/CLongBinary-Class.md) between the field data members of a `CRecordset` object and the columns of a record on the data source of ODBC type **SQL_LONGVARBINARY** or **SQL_LONGVARCHAR**.  
  
## Syntax  
  
```  
  
      void RFX_LongBinary(  
   CFieldExchange* pFX,  
   const char* szName,  
   CLongBinary& value   
);  
```  
  
#### Parameters  
 `pFX`  
 A pointer to an object of class [CFieldExchange](../vs140/CFieldExchange-Class.md). This object contains information to define the context for each call of the function. For more information about the operations a `CFieldExchange` object can specify, see the article [Record Field Exchange: How RFX Works](../vs140/Record-Field-Exchange--How-RFX-Works.md).  
  
 `szName`  
 The name of a data column.  
  
 *value*  
 The value stored in the indicated data member — the value to be transferred. For a transfer from recordset to data source, the value, of type `CLongBinary`, is taken from the specified data member. For a transfer from data source to recordset, the value is stored in the specified data member.  
  
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
 [RFX_Binary](../vs140/RFX_Binary.md)   
 [CFieldExchange::SetFieldType](../vs140/CFieldExchange--SetFieldType.md)   
 [CLongBinary Class](../vs140/CLongBinary-Class.md)