---
title: "CDBVariant::m_dblVal"
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
ms.topic: reference
ms.assetid: 6da6cb88-1313-45a4-a661-b3fa3279b378
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDBVariant::m_dblVal
Stores a value of type **double**.  
  
## Remarks  
 The **m_dblVal** data member belongs to a union. Before accessing **m_dblVal**, first check the value of [CDBVariant::m_dwType](../vs140/CDBVariant--m_dwType.md). If `m_dwType` is set to **DBVT_DOUBLE**, then **m_dblVal** contains a valid value; otherwise, accessing **m_dblVal** will produce unreliable results.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDBVariant Class](../vs140/CDBVariant-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDBVariant::m_dwType](../vs140/CDBVariant--m_dwType.md)