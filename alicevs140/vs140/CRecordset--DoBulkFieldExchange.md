---
title: "CRecordset::DoBulkFieldExchange"
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
ms.assetid: bdd9b9bd-aa94-4a22-b733-e44cc7efa9f9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::DoBulkFieldExchange
Called to exchange bulk rows of data from the data source to the recordset. Implements bulk record field exchange (Bulk RFX).  
  
## Syntax  
  
```  
  
      virtual void DoBulkFieldExchange(   
   CFieldExchange* pFX    
);  
```  
  
#### Parameters  
 `pFX`  
 A pointer to a [CFieldExchange](../vs140/CFieldExchange-Class.md) object. The framework will already have set up this object to specify a context for the field exchange operation.  
  
## Remarks  
 When bulk row fetching is implemented, the framework calls this member function to automatically transfer data from the data source to your recordset object. `DoBulkFieldExchange` also binds your parameter data members, if any, to parameter placeholders in the SQL statement string for the recordset's selection.  
  
 If bulk row fetching is not implemented, the framework calls [DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md). To implement bulk row fetching, you must specify the `CRecordset::useMultiRowFetch` option of the `dwOptions` parameter in the [Open](../vs140/CRecordset--Open.md) member function.  
  
> [!NOTE]
>  `DoBulkFieldExchange` is available only if you are using a class derived from `CRecordset`. If you have created a recordset object directly from `CRecordset`, you must call the [GetFieldValue](../vs140/CRecordset--GetFieldValue.md) member function to retrieve data.  
  
 Bulk record field exchange (Bulk RFX) is similar to record field exchange (RFX). Data is automatically transferred from the data source to the recordset object. However, you cannot call `AddNew`, **Edit**, **Delete**, or **Update** to transfer changes back to the data source. Class `CRecordset` currently does not provide a mechanism for updating bulk rows of data; however, you can write your own functions by using the ODBC API function **SQLSetPos**.  
  
 Note that ClassWizard does not support bulk record field exchange; therefore, you must override `DoBulkFieldExchange` manually by writing calls to the Bulk RFX functions. For more information about these functions, see the topic [Record Field Exchange Functions](../vs140/Record-Field-Exchange-Functions.md).  
  
 For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md). For related information, see the article [Record Field Exchange (RFX)](../vs140/Record-Field-Exchange--RFX-.md).  
  
## Exceptions  
 This method can throw exceptions of type **CDBException\***.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::m_nFields](../vs140/CRecordset--m_nFields.md)   
 [CRecordset::m_nParams](../vs140/CRecordset--m_nParams.md)   
 [CRecordset::DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md)   
 [CRecordset::GetFieldValue](../vs140/CRecordset--GetFieldValue.md)   
 [CFieldExchange Class](../vs140/CFieldExchange-Class.md)   
 [Record Field Exchange Functions](../vs140/Record-Field-Exchange-Functions.md)