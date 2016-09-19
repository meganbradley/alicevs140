---
title: "RFX_Date"
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
ms.assetid: 0588113d-133c-4f99-8603-9f7722be20ee
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RFX_Date
Transfers `CTime` or **TIMESTAMP_STRUCT** data between the field data members of a `CRecordset` object and the columns of a record on the data source of ODBC type **SQL_DATE**, **SQL_TIME**, or **SQL_TIMESTAMP**.  
  
## Syntax  
  
```  
  
      void RFX_Date(  
   CFieldExchange* pFX,  
   const char* szName,  
   CTime& value   
);  
void RFX_Date(  
   CFieldExchange* pFX,  
   const char* szName,  
   TIMESTAMP_STRUCT& value   
);  
void RFX_Date(  
   CFieldExchange* pFX,  
   const char* szName,  
   COleDateTime& value   
);  
```  
  
#### Parameters  
 `pFX`  
 A pointer to an object of class [CFieldExchange](../vs140/CFieldExchange-Class.md). This object contains information to define the context for each call of the function. For more information about the operations a `CFieldExchange` object can specify, see the article [Record Field Exchange: How RFX Works](../vs140/Record-Field-Exchange--How-RFX-Works.md).  
  
 `szName`  
 The name of a data column.  
  
 *value*  
 The value stored in the indicated data member; the value to be transferred. The various versions of the function take different data types for value:  
  
 The first version of the function takes a reference to a [CTime](../Topic/CTime%20Class.md) object. For a transfer from recordset to data source, this value is taken from the specified data member. For a transfer from data source to recordset, the value is stored in the specified data member.  
  
 The second version of the function takes a reference to a **TIMESTAMP_STRUCT** structure. You must set up this structure yourself before the call. Neither dialog data exchange (DDX) support nor code wizard support is available for this version. The third version of the function works similarly to the first version except that it takes a reference to a [COleDateTime](../vs140/COleDateTime-Class.md) object.  
  
## Remarks  
 The `CTime` version of the function imposes the overhead of some intermediate processing and has a somewhat limited range. If you find either of these factors too limiting, use the second version of the function. But note its lack of code wizard and DDX support and the requirement that you set up the structure yourself.  
  
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
 [RFX_Byte](../vs140/RFX_Byte.md)   
 [RFX_Binary](../vs140/RFX_Binary.md)   
 [RFX_LongBinary](../vs140/RFX_LongBinary.md)   
 [CFieldExchange::SetFieldType](../vs140/CFieldExchange--SetFieldType.md)