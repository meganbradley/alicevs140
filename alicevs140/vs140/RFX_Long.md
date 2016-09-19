---
title: "RFX_Long"
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
ms.assetid: 99540206-3794-4393-986e-5d6b7a7ac7b1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RFX_Long
Transfers long integer data between the field data members of a `CRecordset` object and the columns of a record on the data source of ODBC type **SQL_INTEGER**.  
  
## Syntax  
  
```  
  
      void RFX_Long(  
   CFieldExchange* pFX,  
   const char* szName,  
   LONG&   
value );  
```  
  
#### Parameters  
 `pFX`  
 A pointer to an object of class [CFieldExchange](../vs140/CFieldExchange-Class.md). This object contains information to define the context for each call of the function. For more information about the operations a `CFieldExchange` object can specify, see the article [Record Field Exchange: How RFX Works](../vs140/Record-Field-Exchange--How-RFX-Works.md).  
  
 `szName`  
 The name of a data column.  
  
 *value*  
 The value stored in the indicated data member — the value to be transferred. For a transfer from recordset to data source, the value, of type **long**, is taken from the specified data member. For a transfer from data source to recordset, the value is stored in the specified data member.  
  
## Example  
 See [RFX_Text](../vs140/RFX_Text.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [RFX_Text](../vs140/RFX_Text.md)   
 [RFX_Bool](../vs140/RFX_Bool.md)   
 [RFX_Int](../vs140/RFX_Int.md)   
 [RFX_Single](../vs140/RFX_Single.md)   
 [RFX_Double](../vs140/RFX_Double.md)   
 [RFX_Date](../vs140/RFX_Date.md)   
 [RFX_Byte](../vs140/RFX_Byte.md)   
 [RFX_Binary](../vs140/RFX_Binary.md)   
 [RFX_LongBinary](../vs140/RFX_LongBinary.md)   
 [CFieldExchange::SetFieldType](../vs140/CFieldExchange--SetFieldType.md)