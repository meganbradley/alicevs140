---
title: "CRecordset::DoFieldExchange"
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
ms.assetid: 197fb2fb-7752-4830-8188-589b4d4ce7e8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::DoFieldExchange
Called to exchange data (in both directions) between the field data members of the recordset and the corresponding record on the data source. Implements record field exchange (RFX).  
  
## Syntax  
  
```  
  
      virtual void DoFieldExchange(   
   CFieldExchange* pFX    
);  
```  
  
#### Parameters  
 `pFX`  
 A pointer to a [CFieldExchange](../vs140/CFieldExchange-Class.md) object. The framework will already have set up this object to specify a context for the field exchange operation.  
  
## Remarks  
 When bulk row fetching is not implemented, the framework calls this member function to automatically exchange data between the field data members of your recordset object and the corresponding columns of the current record on the data source. `DoFieldExchange` also binds your parameter data members, if any, to parameter placeholders in the SQL statement string for the recordset's selection.  
  
 If bulk row fetching is implemented, the framework calls [DoBulkFieldExchange](../vs140/CRecordset--DoBulkFieldExchange.md). To implement bulk row fetching, you must specify the `CRecordset::useMultiRowFetch` option of the `dwOptions` parameter in the [Open](../vs140/CRecordset--Open.md) member function.  
  
> [!NOTE]
>  `DoFieldExchange` is available only if you are using a class derived from `CRecordset`. If you have created a recordset object directly from `CRecordset`, you must call the [GetFieldValue](../vs140/CRecordset--GetFieldValue.md) member function to retrieve data.  
  
 The exchange of field data, called record field exchange (RFX), works in both directions: from the recordset object's field data members to the fields of the record on the data source, and from the record on the data source to the recordset object.  
  
 The only action you must normally take to implement `DoFieldExchange` for your derived recordset class is to create the class with ClassWizard and specify the names and data types of the field data members. You might also add code to what ClassWizard writes to specify parameter data members or to deal with any columns you bind dynamically. For more information, see the article [Recordset: Dynamically Binding Data Columns (ODBC)](../vs140/Recordset--Dynamically-Binding-Data-Columns--ODBC-.md).  
  
 When you declare your derived recordset class with ClassWizard, the wizard writes an override of `DoFieldExchange` for you, which resembles the following example:  
  
 [!CODE [NVC_MFCDatabase#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#19)]  
  
 For more information about the RFX functions, see the topic [Record Field Exchange Functions](../vs140/Record-Field-Exchange-Functions.md).  
  
 For further examples and details about `DoFieldExchange`, see the article [Record Field Exchange: How RFX Works](../vs140/Record-Field-Exchange--How-RFX-Works.md). For general information about RFX, see the article [Record Field Exchange](../vs140/Record-Field-Exchange--RFX-.md).  
  
## Exceptions  
 This method can throw exceptions of type **CDBException\***.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::m_nFields](../vs140/CRecordset--m_nFields.md)   
 [CRecordset::m_nParams](../vs140/CRecordset--m_nParams.md)   
 [CRecordset::DoBulkFieldExchange](../vs140/CRecordset--DoBulkFieldExchange.md)   
 [CRecordset::GetFieldValue](../vs140/CRecordset--GetFieldValue.md)   
 [CFieldExchange Class](../vs140/CFieldExchange-Class.md)   
 [Record Field Exchange Functions](../vs140/Record-Field-Exchange-Functions.md)