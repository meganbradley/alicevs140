---
title: "IRowsetImpl::AddRefRows"
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
ms.assetid: adc0989b-7592-432e-82d9-df4445431531
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetImpl::AddRefRows
Adds a reference count to an existing row handle.  
  
## Syntax  
  
```  
  
      STDMETHOD( AddRefRows )(  
   DBCOUNTITEM cRows,  
   const HROW rghRows[],  
   DBREFCOUNT rgRefCounts[],  
   DBROWSTATUS rgRowStatus[]   
);  
```  
  
#### Parameters  
 See [IRowset::AddRefRows](https://msdn.microsoft.com/en-us/library/ms719619.aspx) in the *OLE DB Programmer's Reference*.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IRowsetImpl Class](../vs140/IRowsetImpl-Class.md)   
 [IRowsetImpl::RefRows](../vs140/IRowsetImpl--RefRows.md)   
 [IRowsetImpl::GetNextRows](../vs140/IRowsetImpl--GetNextRows.md)   
 [IRowsetImpl::ReleaseRows](../vs140/IRowsetImpl--ReleaseRows.md)