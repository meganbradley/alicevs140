---
title: "IRowsetInfoImpl::GetProperties"
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
ms.assetid: 62c12063-28e0-4a06-ad4d-21c5c1e9ccea
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetInfoImpl::GetProperties
Returns the current settings for properties in the **DBPROPSET_ROWSET** group.  
  
## Syntax  
  
```  
  
      STDMETHOD ( GetProperties )(  
   const ULONG cPropertyIDSets,  
   const DBPROPIDSET rgPropertyIDSets[],  
   ULONG* pcPropertySets,  
   DBPROPSET** prgPropertySets   
);  
```  
  
#### Parameters  
 See [IRowsetInfo::GetProperties](https://msdn.microsoft.com/en-us/library/ms719611.aspx) in the *OLE DB Programmer's Reference*.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IRowsetInfoImpl Class](../vs140/IRowsetInfoImpl-Class.md)   
 [IRowsetInfoImpl::GetReferencedRowset](../vs140/IRowsetInfoImpl--GetReferencedRowset.md)   
 [IRowsetInfoImpl::GetSpecification](../vs140/IRowsetInfoImpl--GetSpecification.md)