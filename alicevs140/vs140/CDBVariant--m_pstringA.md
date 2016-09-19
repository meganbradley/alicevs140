---
title: "CDBVariant::m_pstringA"
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
ms.assetid: d6c95e70-5e03-40f3-8bac-658b1973e904
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDBVariant::m_pstringA
Stores a pointer to an ASCII [CString](../vs140/CStringT-Class.md) object.  
  
## Remarks  
 The **m_pstringA** data member belongs to a union. Before accessing **m_pstringA**, first check the value of [CDBVariant::m_dwType](../vs140/CDBVariant--m_dwType.md). If `m_dwType` is set to **DBVT_ASTRING**, then **m_pstringA** contains a valid pointer; otherwise, accessing **m_pstringA** will produce unreliable results.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDBVariant Class](../vs140/CDBVariant-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDBVariant::m_dwType](../vs140/CDBVariant--m_dwType.md)