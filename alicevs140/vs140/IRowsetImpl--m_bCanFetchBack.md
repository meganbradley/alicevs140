---
title: "IRowsetImpl::m_bCanFetchBack"
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
ms.assetid: cfa007b0-7ba5-48a3-9d05-9f1916305fb7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetImpl::m_bCanFetchBack
Indicates whether a provider supports backward fetching.  
  
## Syntax  
  
```  
  
unsigned m_bCanFetchBack:1;  
  
```  
  
## Remarks  
 Linked to the **DBPROP_CANFETCHBACKWARDS** property in the **DBPROPSET_ROWSET** group. The provider must support **DBPROP_CANFETCHBACKWARDS** for **m_bCanFetchBackwards** to be true.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IRowsetImpl Class](../vs140/IRowsetImpl-Class.md)   
 [IRowsetImpl::m_bCanScrollBack](../vs140/IRowsetImpl--m_bCanScrollBack.md)