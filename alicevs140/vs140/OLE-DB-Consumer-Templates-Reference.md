---
title: "OLE DB Consumer Templates Reference"
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
ms.assetid: cfc7f698-1a0e-4a09-a4d3-ccb99e6654fe
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OLE DB Consumer Templates Reference
The OLE DB Consumer Templates contain the following classes. The reference material also includes topics on the [macros for OLE DB Consumer Templates](../vs140/Macros-and-Global-Functions-for-OLE-DB-Consumer-Templates.md).  
  
## Session Classes  
 [CDataConnection](../vs140/CDataConnection-Class.md)  
 Manages the connection with the data source. This is a useful class for creating clients because it encapsulates necessary objects (data source and session) and some of the work you need to do when connecting to a data source.  
  
 [CDataSource](../vs140/CDataSource-Class.md)  
 Corresponds to an OLE DB data source object, representing a connection through a provider to a data source. One or more database sessions, each represented by a `CSession` object, can take place on a single connection.  
  
 [CEnumerator](../vs140/CEnumerator-Class.md)  
 Corresponds to an OLE DB enumerator object, which retrieves rowset information about available data sources.  
  
 [CEnumeratorAccessor](../vs140/CEnumeratorAccessor-Class.md)  
 Used by `CEnumerator` to access the data from the enumerator rowset. This rowset consists of the data sources and enumerators visible from the current enumerator.  
  
 [CSession](../vs140/CSession-Class.md)  
 Represents a single database access session. One or more sessions can be associated with each `CDataSource` object.  
  
## Accessor Classes  
 [CAccessor](../vs140/CAccessor-Class.md)  
 Used for records that are statically bound to a data source. Use this accessor class when you know the structure of the data source.  
  
 [CAccessorBase](../vs140/CAccessorBase-Class.md)  
 Base class for all accessor classes.  
  
 [CDynamicAccessor](../vs140/CDynamicAccessor-Class.md)  
 An accessor that can be created at run time, based on the column information of the rowset. Use this class to retrieve data if you do not know the structure of the data source.  
  
 [CDynamicParameterAccessor](../vs140/CDynamicParameterAccessor-Class.md)  
 An accessor that can be used when command types are unknown. Obtains the parameter information by calling the `ICommandWithParameters` interface, if the provider supports the interface.  
  
 [CDynamicStringAccessor](../vs140/CDynamicStringAccessor-Class.md)  
 Allows you to access a data source when you have no knowledge of the database's underlying structure.  
  
 [CDynamicStringAccessorA](../vs140/CDynamicStringAccessorA-Class.md)  
 Similar to `CDynamicStringAccessor` except that this class requests data accessed from the data store as ANSI string data.  
  
 [CDynamicStringAccessorW](../vs140/CDynamicStringAccessorW-Class.md)  
 Similar to `CDynamicStringAccessor` except that this class requests data accessed from the data store as UNICODE string data.  
  
 [CManualAccessor](../vs140/CManualAccessor-Class.md)  
 An accessor with methods to handle both columns and command parameters. With this class, you can use any data types as long as the provider can convert the type.  
  
 [CNoAccessor](../vs140/CNoAccessor-Class.md)  
 Can be used as a template argument when you do not want the class to support parameters or output columns.  
  
 [CXMLAccessor](../vs140/CXMLAccessor-Class.md)  
 Similar to `CDynamicStringAccessor` except that this class converts all data accessed from the data store as XML-formatted (tagged) data.  
  
## Rowset Classes  
 [CAccessorRowset](../vs140/CAccessorRowset-Class.md)  
 Encapsulates a rowset and its associated accessors.  
  
 [CArrayRowset](../vs140/CArrayRowset-Class.md)  
 Used to access elements of a rowset using array syntax.  
  
 [CBulkRowset](../vs140/CBulkRowset-Class.md)  
 Used to fetch and manipulate rows in bulk by retrieving multiple row handles with a single call.  
  
 [CNoRowset](../vs140/CNoRowset-Class.md)  
 Can be used as a template argument if the command does not return a rowset.  
  
 [CRestrictions](../vs140/CRestrictions-Class.md)  
 Used to specify restrictions for schema rowsets.  
  
 [CRowset](../vs140/CRowset-Class.md)  
 Used to manipulate, set, and retrieve rowset data.  
  
 [CStreamRowset](../vs140/CStreamRowset-Class.md)  
 Returns an `ISequentialStream` object rather than a rowset; you then use the **Read** method to retrieve data in XML format. (SQL Server 2000 does the formatting; note that this feature works with SQL Server 2000 only.)  
  
 [IRowsetNotifyImpl](../vs140/IRowsetNotifyImpl-Class.md)  
 Provides a dummy implementation for `IRowsetNotify`, with empty functions for the `IRowsetNotify` methods `OnFieldChange`, `OnRowChange`, and `OnRowsetChange`.  
  
 [Schema Rowset Classes and Typedef Classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md)  
  
 The OLE DB Templates provide you with a set of classes that correspond to the OLE DB schema rowsets.  
  
## Command Classes  
 [CCommand](../vs140/CCommand-Class.md)  
 Used to set and execute a parameter-based OLE DB command. To merely open a simple rowset, use `CTable` instead.  
  
 [CMultipleResults](../vs140/CMultipleResults-Class.md)  
 Used as a template argument for the `CCommand` template when you want the command to handle multiple result sets.  
  
 [CNoAccessor](../vs140/CNoAccessor-Class.md)  
 Used as a template argument for template classes, such as `CCommand` and `CTable`, that take an accessor class argument. Use `CNoAccessor` if you do not want the class to support parameters or output columns.  
  
 [CNoMultipleResults](../vs140/CNoMultipleResults-Class.md)  
 Used as a template argument for the `CCommand` template when you want the command to handle a single rowset. `CNoMultipleResults` is the default value for the template argument.  
  
 [CNoRowset](../vs140/CNoRowset-Class.md)  
 Used as a template argument for `CCommand` or `CTable` if the command or table does not return a rowset.  
  
 [CTable](../vs140/CTable-Class.md)  
 Used to access a simple rowset with no parameters.  
  
## Property Classes  
 [CDBPropIDSet](../vs140/CDBPropIDSet-Class.md)  
 Used to pass an array of property IDs for which the consumer wants property information. The properties belong to one property set.  
  
 [CDBPropSet](../vs140/CDBPropSet-Class.md)  
 Used to set properties on a provider.  
  
## Bookmark Class  
 [CBookmark](../vs140/CBookmark-Class.md)  
 Used as an index for accessing data in a rowset.  
  
## Error Class  
 [CDBErrorInfo](../vs140/CDBErrorInfo-Class.md)  
 Used to retrieve OLE DB error information.  
  
## See Also  
 [OLE DB Provider Templates Reference](../vs140/OLE-DB-Provider-Templates-Reference.md)   
 [OLE DB Templates](../vs140/OLE-DB-Templates.md)