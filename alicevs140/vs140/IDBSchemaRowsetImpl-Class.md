---
title: "IDBSchemaRowsetImpl Class"
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
ms.assetid: bd7bf0d7-a1c6-4afa-88e3-cfdbdf560703
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDBSchemaRowsetImpl Class
Provides implementation for schema rowsets.  
  
## Syntax  
  
```  
template <class SessionClass>  
class ATL_NO_VTABLE IDBSchemaRowsetImpl : public IDBSchemaRowset  
```  
  
#### Parameters  
 `SessionClass`  
 The class by which `IDBSchemaRowsetImpl` is inherited. Typically, this class will be the user's session class.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[CheckRestrictions](../vs140/IDBSchemaRowsetImpl--CheckRestrictions.md)|Checks the validity of restrictions against a schema rowset.|  
|[CreateSchemaRowset](../vs140/IDBSchemaRowsetImpl--CreateSchemaRowset.md)|Implements a COM object creator function for the object specified by the template parameter.|  
|[SetRestrictions](../vs140/IDBSchemaRowsetImpl--SetRestrictions.md)|Specifies which restrictions you support on a particular schema rowset.|  
  
### Interface Methods  
  
|||  
|-|-|  
|[GetRowset](../vs140/IDBSchemaRowsetImpl--GetRowset.md)|Returns a schema rowset.|  
|[GetSchemas](../vs140/IDBSchemaRowsetImpl--GetSchemas.md)|Returns a list of schema rowsets accessible by [IDBSchemaRowsetImpl::GetRowset](../vs140/IDBSchemaRowsetImpl--GetRowset.md).|  
  
## Remarks  
 This class implements the [IDBSchemaRowset](https://msdn.microsoft.com/en-us/library/ms713686.aspx) interface and the templatized creator function [CreateSchemaRowset](../vs140/IDBSchemaRowsetImpl--CreateSchemaRowset.md).  
  
 OLE DB uses schema rowsets to return data about the data in a provider. Such data is often called "metadata." By default, a provider must always support `DBSCHEMA_TABLES`, **DBSCHEMA_COLUMNS**, and **DBSCHEMA_PROVIDER_TYPES**, as described in [IDBSchemaRowset](https://msdn.microsoft.com/en-us/library/ms713686.aspx) in the *OLE DB Programmer's Reference*. Schema rowsets are designated in a schema map. For information about the schema map entries, see [SCHEMA_ENTRY](../vs140/SCHEMA_ENTRY.md).  
  
 The OLE DB Provider Wizard, in the ATL Object Wizard, automatically generates code for the schema rowsets in your project. (By default, the wizard supports the mandatory schema rowsets previously mentioned.) When you create a consumer using the ATL Object Wizard, the wizard uses schema rowsets to bind the correct data to a provider. If you do not implement your schema rowsets to provide the correct metadata, the wizard will not bind the correct data.  
  
 For information on how to support schema rowsets in your provider, see [Supporting Schema Rowsets](../vs140/Supporting-Schema-Rowsets.md).  
  
 For more information about schema rowsets, see [Schema Rowsets](https://msdn.microsoft.com/en-us/library/ms712921.aspx) in the *OLE DB Programmer's Reference*.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IDBSchemaRowsetImpl Class Members](assetId:///e74f6f82-541c-42e7-b4c6-e2d4656a0649)   
 [Schema Rowset Classes and Typedef Classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md)   
 [Supporting Schema Rowsets](../vs140/Supporting-Schema-Rowsets.md)