---
title: "IColumnsInfoImpl Class"
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
ms.assetid: ba74c1c5-2eda-4452-8b57-84919fa0d066
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IColumnsInfoImpl Class
Provides an implementation of the [IColumnsInfo](https://msdn.microsoft.com/en-us/library/ms724541.aspx) interface.  
  
## Syntax  
  
```  
template <class T>  
class ATL_NO_VTABLE IColumnsInfoImpl :   
   public IColumnsInfo,    
   public CDBIDOps  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IColumnsInfoImpl`.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[GetColumnInfo](../vs140/IColumnsInfoImpl--GetColumnInfo.md)|Returns the column metadata needed by most consumers.|  
|[MapColumnIDs](../vs140/IColumnsInfoImpl--MapColumnIDs.md)|Returns an array of ordinals of the columns in a rowset that are identified by the specified column IDs.|  
  
## Remarks  
 A mandatory interface on rowsets and commands. To modify the behavior of your provider's `IColumnsInfo` implementation, you need to modify the provider column map.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)