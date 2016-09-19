---
title: "IRowsetIdentityImpl Class"
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
ms.assetid: 56821edf-e045-40c8-96bd-231552cd5799
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetIdentityImpl Class
Implements the OLE DB [IRowsetIdentity](https://msdn.microsoft.com/en-us/library/ms715913.aspx) interface, which enables testing for row identity.  
  
## Syntax  
  
```  
template <class T, class RowClass = CSimpleRow>  
class ATL_NO_VTABLE IRowsetIdentityImpl   
   : public IRowsetIdentity  
```  
  
#### Parameters  
 `T`  
 A class derived from `IRowsetIdentityImpl`.  
  
 `RowClass`  
 The storage unit for the **HROW**.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[IsSameRow](../vs140/IRowsetIdentityImpl--IsSameRow.md)|Compares two row handles to see if they refer to the same row.|  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)