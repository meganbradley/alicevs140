---
title: "CRecordset::m_nFields"
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
ms.assetid: ee7088af-bd8a-4984-81d3-897910d492b5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::m_nFields
Contains the number of field data members in the recordset class; that is, the number of columns selected by the recordset from the data source.  
  
## Remarks  
 The constructor for the recordset class must initialize `m_nFields` with the correct number. If you have not implemented bulk row fetching, ClassWizard writes this initialization for you when you use it to declare your recordset class. You can also write it manually.  
  
 The framework uses this number to manage interaction between the field data members and the corresponding columns of the current record on the data source.  
  
> [!CAUTION]
>  This number must correspond to the number of "output columns" registered in `DoFieldExchange` or `DoBulkFieldExchange` after a call to [SetFieldType](../vs140/CFieldExchange--SetFieldType.md) with the parameter **CFieldExchange::outputColumn**.  
  
 You can bind columns dynamically, as explained in the article "Recordset: Dynamically Binding Data Columns." If you do so, you must increase the count in `m_nFields` to reflect the number of RFX or Bulk RFX function calls in your `DoFieldExchange` or `DoBulkFieldExchange` member function for the dynamically bound columns.  
  
 For more information, see the articles [Recordset: Dynamically Binding Data Columns (ODBC)](../vs140/Recordset--Dynamically-Binding-Data-Columns--ODBC-.md) and [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
## Example  
 See the article [Record Field Exchange: Using RFX](../vs140/Record-Field-Exchange--Using-RFX.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md)   
 [CRecordset::DoBulkFieldExchange](../vs140/CRecordset--DoBulkFieldExchange.md)   
 [CRecordset::m_nParams](../vs140/CRecordset--m_nParams.md)   
 [CFieldExchange::SetFieldType](../vs140/CFieldExchange--SetFieldType.md)