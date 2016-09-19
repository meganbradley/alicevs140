---
title: "CDBVariant::m_chVal"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 01cef6ae-4f84-412b-9a8e-6cf9da0568a7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDBVariant::m_chVal
Stores a value of type `unsigned char`.  
  
## Remarks  
 The **m_chVal** data member belongs to a union. Before accessing **m_chVal**, first check the value of [CDBVariant::m_dwType](../vs140/CDBVariant--m_dwType.md). If `m_dwType` is set to **DBVT_UCHAR**, then **m_chVal** contains a valid value; otherwise, accessing **m_chVal** will produce unreliable results.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDBVariant Class](../vs140/CDBVariant-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDBVariant::m_dwType](../vs140/CDBVariant--m_dwType.md)