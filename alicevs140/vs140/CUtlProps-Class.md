---
title: "CUtlProps Class"
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
ms.assetid: bb525178-765c-4e23-a110-c0fd70c05437
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUtlProps Class
Implements properties for a variety of OLE DB property interfaces (for example, `IDBProperties`, `IDBProperties`, and `IRowsetInfo`).  
  
## Syntax  
  
```  
template < class T >  
class ATL_NO_VTABLE CUtlProps : public CUtlPropsBase  
```  
  
#### Parameters  
 `T`  
 The class that contains the `BEGIN_PROPSET_MAP`.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[GetPropValue](../vs140/CUtlProps--GetPropValue.md)|Gets a property from a property set.|  
|[IsValidValue](../vs140/CUtlProps--IsValidValue.md)|Used to validate a value before setting a property.|  
|[OnInterfaceRequested](../vs140/CUtlProps--OnInterfaceRequested.md)|Handles requests for an optional interface when a consumer calls a method on an object creation interface.|  
|[OnPropertyChanged](../vs140/CUtlProps--OnPropertyChanged.md)|Called after setting a property to handle chained properties.|  
|[SetPropValue](../vs140/CUtlProps--SetPropValue.md)|Sets a property in a property set.|  
  
## Remarks  
 Most of this class is an implementation detail.  
  
 `CUtlProps` contains two members for setting properties internally: [GetPropValue](../vs140/CUtlProps--GetPropValue.md) and [SetPropValue](../vs140/CUtlProps--SetPropValue.md).  
  
 For more information on the macros used in a property set map, see [BEGIN_PROPSET_MAP](../vs140/BEGIN_PROPSET_MAP.md) and [END_PROPSET_MAP](../vs140/END_PROPSET_MAP.md).  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)