---
title: "IRowsetImpl::m_rgRowHandles"
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
ms.assetid: d3c2578f-58c4-4301-bf59-cf101a523a95
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetImpl::m_rgRowHandles
A map of row handles currently contained by the provider in response to `GetNextRows`.  
  
## Syntax  
  
```  
  
MapClass  
 m_rgRowHandles;  
  
```  
  
## Remarks  
 Row handles are removed by calling `ReleaseRows`. See the [IRowsetImpl overview](../vs140/IRowsetImpl-Class.md) for the definition of *MapClass*.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IRowsetImpl Class](../vs140/IRowsetImpl-Class.md)