---
title: "IRowsetImpl::m_bCanScrollBack"
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
ms.assetid: 69de3179-bf56-415e-935f-e98bcb34debe
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetImpl::m_bCanScrollBack
Indicates whether a provider can have its cursor scroll backwards.  
  
## Syntax  
  
```  
  
unsigned  m_bCanScrollBack:1;  
  
```  
  
## Remarks  
 Linked to the **DBPROP_CANSCROLLBACKWARDS** property in the **DBPROPSET_ROWSET** group. The provider must support **DBPROP_CANSCROLLBACKWARDS** for **m_bCanFetchBackwards** to be true.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IRowsetImpl Class](../vs140/IRowsetImpl-Class.md)   
 [IRowsetImpl::m_bCanFetchBack](../vs140/IRowsetImpl--m_bCanFetchBack.md)