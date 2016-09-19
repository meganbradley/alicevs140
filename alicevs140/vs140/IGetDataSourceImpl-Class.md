---
title: "IGetDataSourceImpl Class"
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
ms.assetid: d63f3178-d663-4f01-8c09-8aab2dd6805a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IGetDataSourceImpl Class
Provides an implementation of the [IGetDataSource](https://msdn.microsoft.com/en-us/library/ms709721.aspx) object.  
  
## Syntax  
  
```  
template <class T>  
class ATL_NO_VTABLE IGetDataSourceImpl : public IGetDataSource  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `IGetDataSourceImpl`.  
  
## Members  
  
### Interface Methods  
  
|||  
|-|-|  
|[GetDataSource](../vs140/IGetDataSourceImpl--GetDataSource.md)|Returns an interface pointer on the data source object that created the session.|  
  
## Remarks  
 This is a mandatory interface on the session for obtaining an interface pointer to the data source object.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)