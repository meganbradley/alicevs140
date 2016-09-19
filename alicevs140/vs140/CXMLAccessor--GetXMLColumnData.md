---
title: "CXMLAccessor::GetXMLColumnData"
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
ms.assetid: 719e8efe-8758-4af7-a855-0e44ea196546
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CXMLAccessor::GetXMLColumnData
Retrieves the column type information of a table as XML-formatted string data, by column.  
  
## Syntax  
  
```  
  
      HRESULT GetXMLColumnData(   
   CSimpleStringW& strOutput    
) throw( );  
```  
  
#### Parameters  
 `strOutput`  
 [out] A reference to a string buffer containing the column type information to be retrieved. The string is formatted with XML tag names that match the data store's column names.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Remarks  
 The following shows how the column type information is formatted in XML. `type` specifies the column's data type. Note that the data types are based on OLE DB data types, not those of the database being accessed.  
  
 `<columninfo>`  
  
 `<column type = I2/> ColumnName`  
  
 `</columninfo>`  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CXMLAccessor Class](../vs140/CXMLAccessor-Class.md)