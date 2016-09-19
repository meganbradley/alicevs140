---
title: "IColumnsInfoImpl::GetColumnInfo"
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
ms.assetid: a6739a39-7402-496a-b544-a5b1ed05fadf
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IColumnsInfoImpl::GetColumnInfo
Returns the column metadata needed by most consumers.  
  
## Syntax  
  
```  
  
      STDMETHOD (GetColumnInfo)(  
   DBORDINAL* pcColumns,  
   DBCOLUMNINFO** prgInfo,  
   OLECHAR** ppStringsBuffer   
);  
```  
  
#### Parameters  
 See [IColumnsInfo::GetColumnInfo](https://msdn.microsoft.com/en-us/library/ms722704.aspx) in the *OLE DB Programmer's Reference*.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IColumnsInfoImpl Class](../vs140/IColumnsInfoImpl-Class.md)   
 [IColumnsInfoImpl::MapColumnIDs](../vs140/IColumnsInfoImpl--MapColumnIDs.md)