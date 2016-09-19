---
title: "Record Field Exchange: Using RFX"
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
ms.assetid: ada8f043-37e6-4d41-9db3-92c997a61957
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Record Field Exchange: Using RFX
This topic explains what you do to use RFX in relation to what the framework does.  
  
> [!NOTE]
>  This topic applies to classes derived from [CRecordset](../vs140/CRecordset-Class.md) in which bulk row fetching has not been implemented. If you are using bulk row fetching, bulk record field exchange (Bulk RFX) is implemented. Bulk RFX is similar to RFX. To understand the differences, see [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
 The following topics contain related information:  
  
-   [Record Field Exchange: Working with the Wizard Code](../vs140/Record-Field-Exchange--Working-with-the-Wizard-Code.md) introduces the main components of RFX and explains the code that the MFC Application Wizard and **Add Class** (as described in [Adding an MFC ODBC Consumer](../vs140/Adding-an-MFC-ODBC-Consumer.md)) write to support RFX and how you might want to modify the wizard code.  
  
-   [Record Field Exchange: Using the RFX Functions](../vs140/Record-Field-Exchange--Using-the-RFX-Functions.md) explains writing calls to the RFX functions in your `DoFieldExchange` override.  
  
 The following table shows your role in relation to what the framework does for you.  
  
### Using RFX: You and the Framework  
  
|You|The framework|  
|---------|-------------------|  
|Declare your recordset classes with a wizard. Specify names and data types of field data members.|The wizard derives a `CRecordset` class and writes a [DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md) override for you, including an RFX function call for each field data member.|  
|(Optional) Manually add any needed parameter data members to the class. Manually add an RFX function call to `DoFieldExchange` for each parameter data member, add a call to [CFieldExchange::SetFieldType](../vs140/CFieldExchange--SetFieldType.md) for the group of parameters, and specify the total number of parameters in [m_nParams](../vs140/CRecordset--m_nParams.md). See [Recordset: Parameterizing a Recordset (ODBC)](../vs140/Recordset--Parameterizing-a-Recordset--ODBC-.md).||  
|(Optional) Manually bind additional columns to field data members. Manually increment [m_nFields](../vs140/CRecordset--m_nFields.md). See [Recordset: Dynamically Binding Data Columns (ODBC)](../vs140/Recordset--Dynamically-Binding-Data-Columns--ODBC-.md).||  
|Construct an object of your recordset class. Before using the object, set the values of its parameter data members, if any.|For efficiency, the framework prebinds the parameters, using ODBC. When you pass parameter values, the framework passes them to the data source. Only the parameter values are sent for requeries, unless the sort and/or filter strings have changed.|  
|Open a recordset object using [CRecordset::Open](../vs140/CRecordset--Open.md).|Executes the recordset's query, binds columns to field data members of the recordset, and calls `DoFieldExchange` to exchange data between the first selected record and the recordset's field data members.|  
|Scroll in the recordset using [CRecordset::Move](../vs140/CRecordset--Move.md) or a menu or toolbar command.|Calls `DoFieldExchange` to transfer data to the field data members from the new current record.|  
|Add, update, and delete records.|Calls `DoFieldExchange` to transfer data to the data source.|  
  
## See Also  
 [Record Field Exchange (RFX)](../vs140/Record-Field-Exchange--RFX-.md)   
 [Record Field Exchange: How RFX Works](../vs140/Record-Field-Exchange--How-RFX-Works.md)   
 [Recordset: Obtaining SUMs and Other Aggregate Results (ODBC)](../vs140/Recordset--Obtaining-SUMs-and-Other-Aggregate-Results--ODBC-.md)   
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [CFieldExchange Class](../vs140/CFieldExchange-Class.md)   
 [Macros, Global Functions, and Global Variables](../vs140/Macros--Global-Functions--and-Global-Variables.md)