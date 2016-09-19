---
title: "IDBPropertiesImpl::SetProperties"
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
ms.assetid: 2f9fc1de-7f35-4bca-bab3-7b427bf92c26
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDBPropertiesImpl::SetProperties
Sets properties in the Data Source and Initialization property groups, for data source objects, or the Initialization property group, for enumerators.  
  
## Syntax  
  
```  
  
      STDMETHOD(SetProperties)(   
   ULONG cPropertySets,   
   DBPROPSET rgPropertySets[]    
);  
```  
  
#### Parameters  
 See [IDBProperties::SetProperties](https://msdn.microsoft.com/en-us/library/ms723049.aspx) in the *OLE DB Programmer's Reference*.  
  
## Remarks  
 If the provider is initialized, this method sets the values of properties in the **DBPROPSET_DATASOURCE**, **DBPROPSET_DATASOURCEINFO**, **DBPROPSET_DBINIT** property groups for the data source object. If the provider is not initialized, it sets **DBPROPSET_DBINIT** group properties only.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IDBPropertiesImpl Class](../vs140/IDBPropertiesImpl-Class.md)   
 [IDBPropertiesImpl::GetProperties](../vs140/IDBPropertiesImpl--GetProperties.md)   
 [IDBPropertiesImpl::GetPropertyInfo](../vs140/IDBPropertiesImpl--GetPropertyInfo.md)