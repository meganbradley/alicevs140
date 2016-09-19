---
title: "IDBPropertiesImpl Class"
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
ms.assetid: a7f15a8b-95b2-4316-b944-d5d03f8d74ab
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDBPropertiesImpl Class
Provides an implementation for the `IDBProperties` interface.  
  
## Syntax  
  
```  
template <class T>   
class ATL_NO_VTABLE IDBPropertiesImpl   
   : public IDBProperties, public CUtlProps<T>  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IDBPropertiesImpl`.  
  
## Members  
  
### Interface Methods  
  
|||  
|-|-|  
|[GetProperties](../vs140/IDBPropertiesImpl--GetProperties.md)|Returns the values of properties in the Data Source, Data Source Information, and Initialization property groups that are currently set on the data source object or the values of properties in the Initialization property group that are currently set on the enumerator.|  
|[GetPropertyInfo](../vs140/IDBPropertiesImpl--GetPropertyInfo.md)|Returns information about all properties supported by the provider.|  
|[SetProperties](../vs140/IDBPropertiesImpl--SetProperties.md)|Sets properties in the Data Source and Initialization property groups, for data source objects, or the Initialization property group, for enumerators.|  
  
## Remarks  
 [IDBProperties](https://msdn.microsoft.com/en-us/library/ms719607.aspx) is a mandatory interface for data source objects and an optional interface for enumerators. However, if an enumerator exposes [IDBInitialize](https://msdn.microsoft.com/en-us/library/ms713706.aspx), it must expose `IDBProperties`. `IDBPropertiesImpl` implements `IDBProperties` by using a static function defined by [BEGIN_PROPSET_MAP](../vs140/BEGIN_PROPSET_MAP.md).  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)