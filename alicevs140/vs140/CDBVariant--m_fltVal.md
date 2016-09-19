---
title: "CDBVariant::m_fltVal"
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
ms.assetid: 8f6ffa6d-1d8f-4606-9c76-11cd7a4b8b11
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDBVariant::m_fltVal
Stores a value of type **float**.  
  
## Remarks  
 The **m_fltVal** data member belongs to a union. Before accessing **m_fltVal**, first check the value of [CDBVariant::m_dwType](../vs140/CDBVariant--m_dwType.md). If `m_dwType` is set to **DBVT_SINGLE**, then **m_fltVal** contains a valid value; otherwise, accessing **m_fltVal** will produce unreliable results.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDBVariant Class](../vs140/CDBVariant-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDBVariant::m_dwType](../vs140/CDBVariant--m_dwType.md)