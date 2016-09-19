---
title: "CXMLAccessor::GetXMLRowData"
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
ms.assetid: 156b66e3-42fd-491c-8943-38cf5e36f687
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CXMLAccessor::GetXMLRowData
Retrieves the entire contents of a table as XML-formatted string data, by row.  
  
## Syntax  
  
```  
  
      HRESULT GetXMLRowData(   
   CSimpleStringW& strOutput,   
   bool bAppend = false    
) throw( );  
```  
  
#### Parameters  
 `strOutput`  
 [out] A reference to a buffer containing the table data to be retrieved. The data is formatted as string data with XML tag names that match the data store's column names.  
  
 *bAppend*  
 [in] A Boolean value specifying whether to append a string to the end of the output data.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Remarks  
 The following shows how the row data is formatted in XML. `DATA` below represents the row data. Use move methods to move to the desired row.  
  
 `<row>`  
  
 `<column name>DATA</column name>`  
  
 `</row>`  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CXMLAccessor Class](../vs140/CXMLAccessor-Class.md)