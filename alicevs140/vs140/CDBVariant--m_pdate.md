---
title: "CDBVariant::m_pdate"
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
ms.assetid: 958e745e-20bc-4102-bd8c-7493cf4da1d0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDBVariant::m_pdate
Stores a pointer to an object of type **TIMESTAMP_STRUCT**.  
  
## Remarks  
 The **m_pdate** data member belongs to a union. Before accessing **m_pdate**, first check the value of [CDBVariant::m_dwType](../vs140/CDBVariant--m_dwType.md). If `m_dwType` is set to **DBVT_DATE**, then **m_pdate** contains a valid pointer; otherwise, accessing **m_pdate** will produce unreliable results.  
  
 For more information about the **TIMESTAMP_STRUCT** data type, see the topic [C Data Types](https://msdn.microsoft.com/en-us/library/ms714556.aspx) in Appendix D of the *ODBC Programmer's Reference* in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDBVariant Class](../vs140/CDBVariant-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDBVariant::m_dwType](../vs140/CDBVariant--m_dwType.md)