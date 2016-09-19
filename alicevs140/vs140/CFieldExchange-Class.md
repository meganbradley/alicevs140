---
title: "CFieldExchange Class"
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
ms.assetid: 24c5c0b3-06a6-430e-9b6f-005a2c65e29f
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFieldExchange Class
Supports the record field exchange (RFX) and bulk record field exchange (Bulk RFX) routines used by the database classes.  
  
## Syntax  
  
```  
class CFieldExchange  
  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CFieldExchange::IsFieldType](#cfieldexchange__isfieldtype)|Returns nonzero if the current operation is appropriate for the type of field being updated.|  
|[CFieldExchange::SetFieldType](#cfieldexchange__setfieldtype)|Specifies the type of recordset data member — column or parameter — represented by all following calls to RFX functions until the next call to `SetFieldType`.|  
  
## Remarks  
 `CFieldExchange` does not have a base class.  
  
 Use this class if you are writing data exchange routines for custom data types or when you are implementing bulk row fetching; otherwise, you will not directly use this class. RFX and Bulk RFX exchanges data between the field data members of your recordset object and the corresponding fields of the current record on the data source.  
  
> [!NOTE]
>  If you are working with the Data Access Objects (DAO) classes rather than the Open Database Connectivity (ODBC) classes, use class [CDaoFieldExchange](../vs140/CDaoFieldExchange-Class.md) instead. For more information, see the article [Overview:Database Programming](../vs140/Data-Access-Programming--MFC-ATL-.md).  
  
 A `CFieldExchange` object provides the context information needed for record field exchange or bulk record field exchange to take place. `CFieldExchange` objects support a number of operations, including binding parameters and field data members and setting various flags on the fields of the current record. RFX and Bulk RFX operations are performed on recordset-class data members of types defined by the `enum`**FieldType** in `CFieldExchange`. Possible **FieldType** values are:  
  
-   **CFieldExchange::outputColumn** for field data members.  
  
-   **CFieldExchange::inputParam** or **CFieldExchange::param** for input parameter data members.  
  
-   **CFieldExchange::outputParam** for output parameter data members.  
  
-   **CFieldExchange::inoutParam** for input/output parameter data members.  
  
 Most of the class's member functions and data members are provided for writing your own custom RFX routines. You will use `SetFieldType` frequently. For more information, see the articles [Record Field Exchange (RFX)](../vs140/Record-Field-Exchange--RFX-.md) and [Recordset (ODBC)](../vs140/Recordset--ODBC-.md). For information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md). For details about the RFX and Bulk RFX global functions, see [Record Field Exchange Functions](../vs140/Record-Field-Exchange-Functions.md) in the MFC Macros and Globals section of this reference.  
  
## Inheritance Hierarchy  
 `CFieldExchange`  
  
## Requirements  
 **Header:** afxdb.h  
  
##  <a name="cfieldexchange__isfieldtype"></a>  CFieldExchange::IsFieldType  
 If you write your own RFX function, call `IsFieldType` at the beginning of your function to determine whether the current operation can be performed on a particular field or parameter data member type (a **CFieldExchange::outputColumn**, **CFieldExchange::inputParam**, **CFieldExchange::param**, **CFieldExchange::outputParam**, or **CFieldExchange::inoutParam**).  
  
```  
BOOL IsFieldType(    UINT* pnField );  
  
```  
  
### Parameters  
 *pnField*  
 The sequential number of the field or parameter data member is returned in this parameter. This number corresponds to the data member's order in the [CRecordset::DoFieldExchange](../vs140/CRecordset-Class.md#crecordset__dofieldexchange) or [CRecordset::DoBulkFieldExchange](../vs140/CRecordset-Class.md#crecordset__dobulkfieldexchange) function.  
  
### Return Value  
 Nonzero if the current operation can be performed on the current field or parameter type.  
  
### Remarks  
 Follow the model of the existing RFX functions.  
  
##  <a name="cfieldexchange__setfieldtype"></a>  CFieldExchange::SetFieldType  
 You need a call to `SetFieldType` in your recordset class's [DoFieldExchange](../vs140/CRecordset-Class.md#crecordset__dofieldexchange) or [DoBulkFieldExchange](../vs140/CRecordset-Class.md#crecordset__dobulkfieldexchange) override.  
  
```  
void SetFieldType(    UINT nFieldType );  
  
```  
  
### Parameters  
 `nFieldType`  
 A value of the **enum FieldType**, declared in `CFieldExchange`, which can be one of the following:  
  
-   **CFieldExchange::outputColumn**  
  
-   **CFieldExchange::inputParam**  
  
-   **CFieldExchange::param**  
  
-   **CFieldExchange::outputParam**  
  
-   **CFieldExchange::inoutParam**  
  
### Remarks  
 For field data members, you must call `SetFieldType` with a parameter of **CFieldExchange::outputColumn**, followed by calls to the RFX or Bulk RFX functions. If you have not implemented bulk row fetching, then ClassWizard places this `SetFieldType` call for you in the field map section of `DoFieldExchange`.  
  
 If you parameterize your recordset class, you must call `SetFieldType` again, outside any field map section, followed by RFX calls for all the parameter data members. Each type of parameter data member must have its own `SetFieldType` call. The following table distinguishes the different values you can pass to `SetFieldType` to represent the parameter data members of your class:  
  
|SetFieldType parameter value|Type of parameter data member|  
|----------------------------------|-----------------------------------|  
|**CFieldExchange::inputParam**|Input parameter. A value that is passed into the recordset's query or stored procedure.|  
|**CFieldExchange::param**|Same as **CFieldExchange::inputParam**.|  
|**CFieldExchange::outputParam**|Output parameter. A return value of the recordset's stored procedure.|  
|**CFieldExchange::inoutParam**|Input/output parameter. A value that is passed into and returned from the recordset's stored procedure.|  
  
 In general, each group of RFX function calls associated with field data members or parameter data members must be preceded by a call to `SetFieldType`. The `nFieldType` parameter of each `SetFieldType` call identifies the type of the data members represented by the RFX function calls that follow the `SetFieldType` call.  
  
 For more information about handling output and input/output parameters, see the `CRecordset` member function [FlushResultSet](../vs140/CRecordset-Class.md#crecordset__flushresultset). For more information about the RFX and Bulk RFX functions, see the topic [Record Field Exchange Functions](../vs140/Record-Field-Exchange-Functions.md). For related information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
### Example  
 This example shows several calls to RFX functions with accompanying calls to `SetFieldType`. Note that `SetFieldType` is called through the `pFX` pointer to a `CFieldExchange` object.  
  
 [!CODE [NVC_MFCDatabase#33](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#33)]  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset](../vs140/CRecordset-Class.md)