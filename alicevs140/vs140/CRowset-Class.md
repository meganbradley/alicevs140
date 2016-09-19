---
title: "CRowset Class"
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
ms.assetid: b0228a90-b8dd-47cc-b397-8d4c15c1e7f4
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRowset Class
Encapsulates an OLE DB rowset object and several related interfaces and provides manipulation methods for rowset data.  
  
## Syntax  
  
```  
template <class TAccessor = CAccessorBase>  
class CRowset  
```  
  
#### Parameters  
 `TAccessor`  
 An accessor class. The default is `CAccessorBase`.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[AddRefRows](../vs140/CRowset--AddRefRows.md)|Increments the reference count associated with the current row.|  
|[Close](../vs140/CRowset--Close.md)|Releases rows and the current `IRowset` interface.|  
|[Compare](../vs140/CRowset--Compare.md)|Compares two bookmarks using [IRowsetLocate::Compare](https://msdn.microsoft.com/en-us/library/ms709539.aspx).|  
|[CRowset](../vs140/CRowset--CRowset.md)|Creates a new `CRowset` object and (optionally) associates it with an **IRowset** interface supplied as a parameter.|  
|[Delete](../vs140/CRowset--Delete.md)|Deletes rows from the rowset using [IRowsetChange:DeleteRows](https://msdn.microsoft.com/en-us/library/ms724362.aspx).|  
|[FindNextRow](../vs140/CRowset--FindNextRow.md)|Finds the next matching row after the specified bookmark.|  
|[GetApproximatePosition](../vs140/CRowset--GetApproximatePosition.md)|Returns the approximate position of a row corresponding to a bookmark.|  
|[GetData](../vs140/CRowset--GetData.md)|Retrieves data from the rowset's copy of the row.|  
|[GetDataHere](../vs140/CRowset--GetDataHere.md)|Retrieves data from the specified buffer.|  
|[GetOriginalData](../vs140/CRowset--GetOriginalData.md)|Retrieves the data most recently fetched from or transmitted to the data source, ignoring pending changes.|  
|[GetRowStatus](../vs140/CRowset--GetRowStatus.md)|Returns the status of all rows.|  
|[Insert](../vs140/CRowset--Insert.md)|Creates and inserts a new row using [IRowsetChange:InsertRow](https://msdn.microsoft.com/en-us/library/ms716921.aspx).|  
|[IsSameRow](../vs140/CRowset--IsSameRow.md)|Compares the specified row with the current row.|  
|[MoveFirst](../vs140/CRowset--MoveFirst.md)|Repositions the next-fetch location to the initial position.|  
|[MoveLast](../vs140/CRowset--MoveLast.md)|Moves to the last record.|  
|[MoveNext](../vs140/CRowset--MoveNext.md)|Fetches data from the next sequential row or a specified number of positions beyond the next row.|  
|[MovePrev](../vs140/CRowset--MovePrev.md)|Moves to the previous record.|  
|[MoveToBookmark](../vs140/CRowset--MoveToBookmark.md)|Fetches the row marked by a bookmark or the row at a specified offset from that bookmark.|  
|[MoveToRatio](../vs140/CRowset--MoveToRatio.md)|Fetches rows starting from a fractional position in the rowset.|  
|[ReleaseRows](../vs140/CRowset--ReleaseRows.md)|Calls [IRowset::ReleaseRows](https://msdn.microsoft.com/en-us/library/ms719771.aspx) to release the current row handle.|  
|[SetData](../vs140/CRowset--SetData.md)|Sets data values in one or more columns of a row using [IRowsetChange:SetData](https://msdn.microsoft.com/en-us/library/ms721232.aspx).|  
|[Undo](../vs140/CRowset--Undo.md)|Undoes any changes made to a row since the last fetch or [Update](../vs140/CRowset--Update.md).|  
|[Update](../vs140/CRowset--Update.md)|Transmits any pending changes made to the current row since the last fetch or update.|  
|[UpdateAll](../vs140/CRowset--UpdateAll.md)|Transmits any pending changes made to all rows since the last fetch or update.|  
  
## Remarks  
 In OLE DB, a rowset is the object through which a program sets and retrieves data.  
  
 This class is not meant to be instantiated but rather passed as a template parameter to `CTable` or `CCommand` (`CRowset` is the default).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [DBViewer Sample](../vs140/Visual-C---Samples.md)   
 [MultiRead Sample](../vs140/Visual-C---Samples.md)   
 [MultiRead Attributes Sample](../vs140/Visual-C---Samples.md)   
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)