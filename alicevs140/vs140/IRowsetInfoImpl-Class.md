---
title: "IRowsetInfoImpl Class"
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
ms.assetid: 9c654155-7727-464e-bd31-143e68391a47
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetInfoImpl Class
Provides an implementation for the [IRowsetInfo](https://msdn.microsoft.com/en-us/library/ms724541.aspx) interface.  
  
## Syntax  
  
```  
template <class T, class PropClass = T>  
class ATL_NO_VTABLE IRowsetInfoImpl :   
   public IRowsetInfo,    
   public CUtlProps<PropClass>  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IRowsetInfoImpl`.  
  
 `PropClass`  
 A user-definable property class that defaults to `T`.  
  
## Members  
  
### Interface Methods  
  
|||  
|-|-|  
|[GetProperties](../vs140/IRowsetInfoImpl--GetProperties.md)|Returns the current settings of all properties supported by the rowset.|  
|[GetReferencedRowset](../vs140/IRowsetInfoImpl--GetReferencedRowset.md)|Returns an interface pointer to the rowset to which a bookmark applies.|  
|[GetSpecification](../vs140/IRowsetInfoImpl--GetSpecification.md)|Returns an interface pointer on the object (command or session) that created this rowset.|  
  
## Remarks  
 A mandatory interface on rowsets. This class implements the rowset properties by using the [property set map](../vs140/BEGIN_PROPSET_MAP.md) defined in your command class. Although the rowset class appears to be using the command class' property sets, the rowset is supplied with its own copy of the run-time properties, when it is created by a command or session object.  
  
## Requirements  
 **Header:** altdb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)