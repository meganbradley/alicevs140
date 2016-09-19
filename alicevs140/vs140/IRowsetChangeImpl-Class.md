---
title: "IRowsetChangeImpl Class"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1e9fee15-ed9e-4387-af8f-215569beca6c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetChangeImpl Class
The OLE DB Templates implementation of the [IRowsetChange](https://msdn.microsoft.com/en-us/library/ms715790.aspx) interface in the OLE DB specification.  
  
## Syntax  
  
```  
template <  
   class T,   
   class Storage,   
   class BaseInterface = IRowsetChange,   
   class RowClass = CSimpleRow,   
   class MapClass = CAtlMap < RowClass::KeyType, RowClass* >   
>  
class ATL_NO_VTABLE IRowsetChangeImpl : public BaseInterface  
```  
  
#### Parameters  
 `T`  
 A class derived from `IRowsetChangeImpl`.  
  
 `Storage`  
 The user record.  
  
 `BaseInterface`  
 The base class for the interface, such as `IRowsetChange`.  
  
 `RowClass`  
 The storage unit for the row handle.  
  
 `MapClass`  
 The storage unit for all row handles held by the provider.  
  
## Members  
  
### Interface Methods (Used with IRowsetChange)  
  
|||  
|-|-|  
|[DeleteRows](../vs140/IRowsetChangeImpl--DeleteRows.md)|Deletes rows from the rowset.|  
|[InsertRow](../vs140/IRowsetChangeImpl--InsertRow.md)|Inserts a row into the rowset.|  
|[SetData](../vs140/IRowsetChangeImpl--SetData.md)|Sets data values in one or more columns.|  
  
### Implementation Method (Callback)  
  
|||  
|-|-|  
|[FlushData](../vs140/IRowsetChangeImpl--FlushData.md)|Overidden by provider to commit data to its store.|  
  
## Remarks  
 This interface is responsible for immediate write operations to a data store. "Immediate" means that when the end user (the person using the consumer) makes any changes, those changes are immediately transmitted to the data store (and cannot be undone).  
  
 `IRowsetChangeImpl` implements the OLE DB `IRowsetChange` interface, which enables updating of values of columns in existing rows, deleting rows, and inserting new rows.  
  
 The OLE DB Templates implementation supports all the base methods (`SetData`, `InsertRow`, and `DeleteRows`).  
  
> [!IMPORTANT]
>  It is strongly recommended that you read the following documentation BEFORE attempting to implement your provider:  
  
-   [Creating an Updatable Provider](../vs140/Creating-an-Updatable-Provider.md)  
  
-   Chapter 6 of the *OLE DB Programmer's Reference*  
  
-   Also see how the `RUpdateRowset` class is used in the UpdatePV sample  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)