---
title: "CXMLAccessor Class"
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
ms.assetid: c88c082c-ec2f-4351-8947-a330b15e448a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CXMLAccessor Class
Allows you to access data sources as string data when you have no knowledge of the data store's schema (underlying structure).  
  
## Syntax  
  
```  
class CXMLAccessor : public CDynamicStringAccessorW  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[GetXMLColumnData](../vs140/CXMLAccessor--GetXMLColumnData.md)|Retrieves the column information.|  
|[GetXMLRowData](../vs140/CXMLAccessor--GetXMLRowData.md)|Retrieves the entire contents of a table by rows.|  
  
## Remarks  
 However, `CXMLAccessor` differs from `CDynamicStringAccessorW` in that it converts all data accessed from the data store as XML-formatted (tagged) data. This is especially useful for output to XML-aware Web pages. The XML tag names will match the data store's column names as closely as possible.  
  
 Use `CDynamicAccessor` methods to obtain column information. You use this column information to create an accessor dynamically at run time.  
  
 The column information is stored in a buffer created and managed by this class. Obtain column information using [GetXMLColumnData](../vs140/CXMLAccessor--GetXMLColumnData.md) or obtain column data by rows using [GetXMLRowData](../vs140/CXMLAccessor--GetXMLRowData.md).  
  
## Example  
 [!CODE [NVC_OLEDB_Consumer#14](../CodeSnippet/VS_Snippets_Cpp/NVC_OLEDB_Consumer#14)]  
  
## Requirements  
 **Header**: atldbcli.h  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)   
 [CAccessor Class](../vs140/CAccessor-Class.md)   
 [CDynamicAccessor Class](../vs140/CDynamicAccessor-Class.md)   
 [CDynamicParameterAccessor Class](../vs140/CDynamicParameterAccessor-Class.md)   
 [CDynamicStringAccessor Class](../vs140/CDynamicStringAccessor-Class.md)   
 [CDynamicStringAccessorA Class](../vs140/CDynamicStringAccessorA-Class.md)   
 [CDynamicStringAccessorW Class](../vs140/CDynamicStringAccessorW-Class.md)   
 [CManualAccessor Class](../vs140/CManualAccessor-Class.md)