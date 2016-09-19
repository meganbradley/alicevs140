---
title: "CBulkRowset Class"
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
ms.assetid: c6bde426-c543-4022-a98a-9519d9e2ae59
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBulkRowset Class
Fetches and manipulates rows to work on data in bulk by retrieving multiple row handles with a single call.  
  
## Syntax  
  
```  
template <class TAccessor>  
class CBulkRowset : public CRowset<TAccessor>  
```  
  
#### Parameters  
 `TAccessor`  
 An accessor class.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[AddRefRows](../vs140/CBulkRowset--AddRefRows.md)|Increments the reference count.|  
|[CBulkRowset](../vs140/CBulkRowset--CBulkRowset.md)|Constructor.|  
|[MoveFirst](../vs140/CBulkRowset--MoveFirst.md)|Retrieves the first row of data, performing a new bulk fetch if necessary.|  
|[MoveLast](../vs140/CBulkRowset--MoveLast.md)|Moves to the last row.|  
|[MoveNext](../vs140/CBulkRowset--MoveNext.md)|Retrieves the next row of data.|  
|[MovePrev](../vs140/CBulkRowset--MovePrev.md)|Moves to the previous row.|  
|[MoveToBookmark](../vs140/CBulkRowset--MoveToBookmark.md)|Fetches the row marked by a bookmark or the row at a specified offset from that bookmark.|  
|[MoveToRatio](../vs140/CBulkRowset--MoveToRatio.md)|Fetches rows starting from a fractional position in the rowset.|  
|[ReleaseRows](../vs140/CBulkRowset--ReleaseRows.md)|Sets the current row (**m_nCurrentRow**) to zero and releases all rows.|  
|[SetRows](../vs140/CBulkRowset--SetRows.md)|Sets the number of row handles to be retrieved by one call.|  
  
## Example  
 The following example demonstrates use of the `CBulkRowset` class.  
  
 [!CODE [NVC_OLEDB_Consumer#1](../CodeSnippet/VS_Snippets_Cpp/NVC_OLEDB_Consumer#1)]  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)