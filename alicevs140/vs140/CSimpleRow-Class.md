---
title: "CSimpleRow Class"
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
ms.assetid: 06d9621d-60cc-4508-8b0c-528d1b1a809b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleRow Class
Provides a default implementation for the row handle, which is used in the [IRowsetImpl](../vs140/IRowsetImpl-Class.md) class.  
  
## Syntax  
  
```  
class CSimpleRow  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[AddRefRow](../vs140/CSimpleRow--AddRefRow.md)|Adds a reference count to an existing row handle.|  
|[Compare](../vs140/CSimpleRow--Compare.md)|Compares two rows to see if they refer to the same row instance.|  
|[CSimpleRow](../vs140/CSimpleRow--CSimpleRow.md)|The constructor.|  
|[ReleaseRow](../vs140/CSimpleRow--ReleaseRow.md)|Releases rows.|  
  
### Data Members  
  
|||  
|-|-|  
|[m_dwRef](../vs140/CSimpleRow--m_dwRef.md)|Reference count to an existing row handle.|  
|[m_iRowset](../vs140/CSimpleRow--m_iRowset.md)|An index to the rowset representing the cursor.|  
  
## Remarks  
 A row handle is logically a unique tag for a result row. `IRowsetImpl` creates a new `CSimpleRow` for every row requested in [IRowsetImpl::GetNextRows](../vs140/IRowsetImpl--GetNextRows.md). `CSimpleRow` can also be replaced with your own implementation of the row handle, as it is a default template argument to `IRowsetImpl`. The only requirement to replacing this class is to have the replacement class provide a constructor that accepts a single parameter of type **LONG**.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)   
 [IRowsetImpl Class](../vs140/IRowsetImpl-Class.md)