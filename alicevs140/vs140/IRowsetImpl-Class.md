---
title: "IRowsetImpl Class"
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
ms.assetid: 6a9189af-7556-45b1-adcb-9d62bb36704c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetImpl Class
Provides an implementation of the `IRowset` interface.  
  
## Syntax  
  
```  
template <  
   class T,   
   class RowsetInterface,  
   class RowClass = CSimpleRow,  
   class MapClass = CAtlMap <  
      RowClass::KeyType,  
      RowClass*   
   >  
>  
class ATL_NO_VTABLE IRowsetImpl : public RowsetInterface  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IRowsetImpl`.  
  
 `RowsetInterface`  
 A class derived from `IRowsetImpl`.  
  
 `RowClass`  
 Storage unit for the **HROW**.  
  
 `MapClass`  
 Storage unit for all row handles held by the provider.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[AddRefRows](../vs140/IRowsetImpl--AddRefRows.md)|Adds a reference count to an existing row handle.|  
|[CreateRow](../vs140/IRowsetImpl--CreateRow.md)|Called by [GetNextRows](../vs140/IRowsetImpl--GetNextRows.md) to allocate a new **HROW**. Not called directly by user.|  
|[GetData](../vs140/IRowsetImpl--GetData.md)|Retrieves data from the rowset's copy of the row.|  
|[GetDBStatus](../vs140/IRowsetImpl--GetDBStatus.md)|Returns the status for the specified field.|  
|[GetNextRows](../vs140/IRowsetImpl--GetNextRows.md)|Fetches rows sequentially, remembering the previous position.|  
|[IRowsetImpl](../vs140/IRowsetImpl-Class.md)|The constructor. Not called directly by user.|  
|[RefRows](../vs140/IRowsetImpl--RefRows.md)|Called by [AddRefRows](../vs140/IRowsetImpl--AddRefRows.md) and [ReleaseRows](../vs140/IRowsetImpl--ReleaseRows.md). Not called directly by user.|  
|[ReleaseRows](../vs140/IRowsetImpl--ReleaseRows.md)|Releases rows.|  
|[RestartPosition](../vs140/IRowsetImpl--RestartPosition.md)|Repositions the next fetch position to its initial position; that is, its position when the rowset was first created.|  
|[SetDBStatus](../vs140/IRowsetImpl--SetDBStatus.md)|Sets the status flags for the specified field.|  
  
### Data Members  
  
|||  
|-|-|  
|[m_bCanFetchBack](../vs140/IRowsetImpl--m_bCanFetchBack.md)|Indicates whether a provider supports backward fetching.|  
|[m_bCanScrollBack](../vs140/IRowsetImpl--m_bCanScrollBack.md)|Indicates whether a provider can have its cursor scroll backwards.|  
|[m_bReset](../vs140/IRowsetImpl--m_bReset.md)|Indicates whether a provider has reset its cursor position. This has special meaning when scrolling backwards or fetching backwards in [GetNextRows](../vs140/IRowsetImpl--GetNextRows.md).|  
|[m_iRowset](../vs140/IRowsetImpl--m_iRowset.md)|An index to the rowset, representing the cursor.|  
|[m_rgRowHandles](../vs140/IRowsetImpl--m_rgRowHandles.md)|A list of row handles.|  
  
## Remarks  
 [IRowset](https://msdn.microsoft.com/en-us/library/ms720986.aspx) is the base rowset interface.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)