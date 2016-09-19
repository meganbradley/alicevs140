---
title: "ISessionPropertiesImpl::SetProperties"
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
ms.assetid: 2e1219ed-0e1e-460e-84d6-031acfbfd3d2
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ISessionPropertiesImpl::SetProperties
Sets properties in the **DBPROPSET_SESSION** property group.  
  
## Syntax  
  
```  
  
      STDMETHOD(SetProperties)(   
   ULONG cPropertySets,   
   DBPROPSET rgPropertySets[]    
);  
```  
  
#### Parameters  
 See [ISessionProperties::SetProperties](https://msdn.microsoft.com/en-us/library/ms714405.aspx) in the *OLE DB Programmer's Reference*.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [ISessionPropertiesImpl Class](../vs140/ISessionPropertiesImpl-Class.md)   
 [ISessionPropertiesImpl::GetProperties](../vs140/ISessionPropertiesImpl--GetProperties.md)