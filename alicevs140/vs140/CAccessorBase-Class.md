---
title: "CAccessorBase Class"
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
ms.assetid: 389b65be-11ca-4ae0-9290-60c621c4982b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessorBase Class
All accessors in the OLE DB Templates derive from this class. `CAccessorBase` allows one rowset to manage multiple accessors. It also provides binding for both parameters and output columns.  
  
## Syntax  
  
```  
// Replace with syntax  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[Close](../vs140/CAccessorBase--Close.md)|Closes the accessors.|  
|[GetHAccessor](../vs140/CAccessorBase--GetHAccessor.md)|Retrieves the accessor handle.|  
|[GetNumAccessors](../vs140/CAccessorBase--GetNumAccessors.md)|Retrieves the number of accessors created by the class.|  
|[IsAutoAccessor](../vs140/CAccessorBase--IsAutoAccessor.md)|Tests whether the specified accessor is an autoaccessor.|  
|[ReleaseAccessors](../vs140/CAccessorBase--ReleaseAccessors.md)|Releases the accessors.|  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)