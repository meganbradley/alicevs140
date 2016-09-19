---
title: "CDynamicAccessor Class"
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
ms.assetid: 374b13b7-1f09-457d-9e6b-df260ff4d178
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicAccessor Class
Allows you to access a data source when you have no knowledge of the database schema (the database's underlying structure).  
  
## Syntax  
  
```  
class CDynamicAccessor : public CAccessorBase  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[AddBindEntry](../vs140/CDynamicAccessor--AddBindEntry.md)|Adds a bind entry to the output columns when overriding the default accessor.|  
|[CDynamicAccessor](../vs140/CDynamicAccessor-Class.md)|Instantiates and initializes the `CDynamicAccessor` object.|  
|[Close](../vs140/CDynamicAccessor--Close.md)|Unbinds all the columns, releases the allocated memory, and releases the [IAccessor](https://msdn.microsoft.com/en-us/library/ms719672.aspx) interface pointer in the class.|  
|[GetBookmark](../vs140/CDynamicAccessor--GetBookmark.md)|Retrieves the bookmark for the current row.|  
|[GetBlobHandling](../vs140/CDynamicAccessor--GetBlobHandling.md)|Retrieves the BLOB handling value for the current row.|  
|[GetBlobSizeLimit](../vs140/CDynamicAccessor--GetBlobSizeLimit.md)|Retrieves the maximum BLOB size in bytes.|  
|[GetColumnCount](../vs140/CDynamicAccessor--GetColumnCount.md)|Retrieves the number of columns in the rowset.|  
|[GetColumnFlags](../vs140/CDynamicAccessor--GetColumnFlags.md)|Retrieves the column characteristics.|  
|[GetColumnInfo](../vs140/CDynamicAccessor--GetColumnInfo.md)|Retrieves the column metadata.|  
|[GetColumnName](../vs140/CDynamicAccessor--GetColumnName.md)|Retrieves the name of a specified column.|  
|[GetColumnType](../vs140/CDynamicAccessor--GetColumnType.md)|Retrieves the data type of a specified column.|  
|[GetLength](../vs140/CDynamicAccessor--GetLength.md)|Retrieves the maximum possible length of a column in bytes.|  
|[GetOrdinal](../vs140/CDynamicAccessor--GetOrdinal.md)|Retrieves the column index given a column name.|  
|[GetStatus](../vs140/CDynamicAccessor--GetStatus.md)|Retrieves the status of a specified column.|  
|[GetValue](../vs140/CDynamicAccessor--GetValue.md)|Retrieves the data from the buffer.|  
|[SetBlobHandling](../vs140/CDynamicAccessor--SetBlobHandling.md)|Sets the BLOB handling value for the current row.|  
|[SetBlobSizeLimit](../vs140/CDynamicAccessor--SetBlobSizeLimit.md)|Sets the maximum BLOB size in bytes.|  
|[SetLength](../vs140/CDynamicAccessor--SetLength.md)|Sets the length of the column in bytes.|  
|[SetStatus](../vs140/CDynamicAccessor--SetStatus.md)|Sets the status of a specified column.|  
|[SetValue](../vs140/CDynamicAccessor--SetValue.md)|Stores the data to the buffer.|  
  
## Remarks  
 Use `CDynamicAccessor` methods to obtain column information such as column names, column count, data type, and so on. You then use this column information to create an accessor dynamically at run time.  
  
 The column information is stored in a buffer that is created and managed by this class. Obtain data from the buffer using [GetValue](../vs140/CDynamicAccessor--GetValue.md).  
  
 For a discussion and examples of using the dynamic accessor classes, see [Using Dynamic Accessors](../vs140/Using-Dynamic-Accessors.md).  
  
## Requirements  
 **Header**: atldbcli.h  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)   
 [CAccessor Class](../vs140/CAccessor-Class.md)   
 [CDynamicParameterAccessor Class](../vs140/CDynamicParameterAccessor-Class.md)   
 [CManualAccessor Class](../vs140/CManualAccessor-Class.md)