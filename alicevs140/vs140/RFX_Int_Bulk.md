---
title: "RFX_Int_Bulk"
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
ms.assetid: e3ee2eb9-0945-47aa-aed9-250fc39f6dc6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RFX_Int_Bulk
Transfers multiple rows of integer data from a column of an ODBC data source to a corresponding array in a `CRecordset`-derived object.  
  
## Syntax  
  
```  
  
      void RFX_Int_Bulk(  
   CFieldExchange* pFX,  
   LPCTSTR szName,  
   int** prgIntVals,  
   long** prgLengths   
);  
```  
  
#### Parameters  
 `pFX`  
 A pointer to a [CFieldExchange](../vs140/CFieldExchange-Class.md) object. This object contains information to define the context for each call of the function. For more information, see the article [Record Field Exchange: How RFX Works](../vs140/Record-Field-Exchange--How-RFX-Works.md).  
  
 `szName`  
 The name of a data column.  
  
 `prgIntVals`  
 A pointer to an array of integers. This array will store the data to be transferred from the data source to the recordset.  
  
 `prgLengths`  
 A pointer to an array of long integers. This array will store the length in bytes of each value in the array pointed to by `prgIntVals`. Note that the value **SQL_NULL_DATA** will be stored if the corresponding data item contains a Null value. For more details, see the ODBC API function **SQLBindCol** in the *ODBC SDK Programmer's Reference*.  
  
## Remarks  
 The data source column must have an ODBC type of **SQL_SMALLINT**. The recordset must define a field data member of type pointer to `int`.  
  
 If you initialize `prgIntVals` and `prgLengths` to **NULL**, then the arrays they point to will be allocated automatically, with sizes equal to the rowset size.  
  
> [!NOTE]
>  Bulk record field exchange only transfers data from the data source to the recordset object. To make your recordset updateable, you must use the ODBC API function **SQLSetPos**.  
  
 For more information, see the articles [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md) and [Record Field Exchange (RFX)](../vs140/Record-Field-Exchange--RFX-.md).  
  
## Example  
 See [RFX_Text_Bulk](../vs140/RFX_Text_Bulk.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [RFX_Binary_Bulk](../vs140/RFX_Binary_Bulk.md)   
 [RFX_Bool_Bulk](../vs140/RFX_Bool_Bulk.md)   
 [RFX_Byte_Bulk](../vs140/RFX_Byte_Bulk.md)   
 [RFX_Date_Bulk](../vs140/RFX_Date_Bulk.md)   
 [RFX_Double_Bulk](../vs140/RFX_Double_Bulk.md)   
 [RFX_Long_Bulk](../vs140/RFX_Long_Bulk.md)   
 [RFX_Single_Bulk](../vs140/RFX_Single_Bulk.md)   
 [RFX_Text_Bulk](../vs140/RFX_Text_Bulk.md)   
 [CFieldExchange::SetFieldType](../vs140/CFieldExchange--SetFieldType.md)