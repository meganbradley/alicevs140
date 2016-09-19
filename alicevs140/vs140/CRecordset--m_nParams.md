---
title: "CRecordset::m_nParams"
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
ms.assetid: b49ec433-08de-47b5-a9c7-32c50a33b5a1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::m_nParams
Contains the number of parameter data members in the recordset class; that is, the number of parameters passed with the recordset's query.  
  
## Remarks  
 If your recordset class has any parameter data members, the constructor for the class must initialize `m_nParams` with the correct number. The value of `m_nParams` defaults to 0. If you add parameter data members (which you must do manually) you must also manually add an initialization in the class constructor to reflect the number of parameters (which must be at least as large as the number of '?' placeholders in your **m_strFilter** or `m_strSort` string).  
  
 The framework uses this number when it parameterizes the recordset's query.  
  
> [!CAUTION]
>  This number must correspond to the number of "params" registered in `DoFieldExchange` or `DoBulkFieldExchange` after a call to [SetFieldType](../vs140/CFieldExchange--SetFieldType.md) with a parameter value of **CFieldExchange::inputParam**, **CFieldExchange::param**, **CFieldExchange::outputParam**, or **CFieldExchange::inoutParam**.  
  
## Example  
 See the articles [Recordset: Parameterizing a Recordset (ODBC)](../vs140/Recordset--Parameterizing-a-Recordset--ODBC-.md) and [Record Field Exchange: Using RFX](../vs140/Record-Field-Exchange--Using-RFX.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md)   
 [CRecordset::DoBulkFieldExchange](../vs140/CRecordset--DoBulkFieldExchange.md)   
 [CRecordset::m_nFields](../vs140/CRecordset--m_nFields.md)   
 [CFieldExchange::SetFieldType](../vs140/CFieldExchange--SetFieldType.md)