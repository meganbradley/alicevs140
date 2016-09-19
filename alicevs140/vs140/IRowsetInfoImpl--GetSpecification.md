---
title: "IRowsetInfoImpl::GetSpecification"
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
ms.assetid: 8e14289d-9cca-4df7-a9e0-f4ef03c61e30
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetInfoImpl::GetSpecification
Returns an interface pointer on the object (command or session) that created this rowset.  
  
## Syntax  
  
```  
  
      STDMETHOD ( GetSpecification )(  
   REFIID riid,  
   IUnknown** ppSpecification   
);  
```  
  
#### Parameters  
 See [IRowsetInfo::GetSpecification](https://msdn.microsoft.com/en-us/library/ms716746.aspx) in the *OLE DB Programmer's Reference*.  
  
## Remarks  
 Use this method with [IGetDataSourceImpl](../vs140/IGetDataSourceImpl-Class.md) to retrieve properties from the data source object.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IRowsetInfoImpl Class](../vs140/IRowsetInfoImpl-Class.md)   
 [IRowsetInfoImpl::GetReferencedRowset](../vs140/IRowsetInfoImpl--GetReferencedRowset.md)   
 [IRowsetInfoImpl::GetProperties](../vs140/IRowsetInfoImpl--GetProperties.md)