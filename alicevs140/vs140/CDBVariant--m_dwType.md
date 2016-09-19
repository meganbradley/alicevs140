---
title: "CDBVariant::m_dwType"
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
ms.assetid: b80cce28-9b3a-49ee-875d-0cdb49bf1b2d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDBVariant::m_dwType
This data member contains the data type for the value that is currently stored in the `CDBVariant` object's union data member.  
  
## Remarks  
 Before accessing this union, you must check the value of `m_dwType` in order to determine which union data member to access. The following table lists the possible values for `m_dwType` and the corresponding union data member.  
  
|m_dwType|Union data member|  
|---------------|-----------------------|  
|**DBVT_NULL**|No union member is valid for access.|  
|**DBVT_BOOL**|[m_boolVal](../vs140/CDBVariant--m_boolVal.md)|  
|**DBVT_UCHAR**|[m_chVal](../vs140/CDBVariant--m_chVal.md)|  
|**DBVT_SHORT**|[m_iVal](../vs140/CDBVariant--m_iVal.md)|  
|**DBVT_LONG**|[m_lVal](../vs140/CDBVariant--m_lVal.md)|  
|**DBVT_SINGLE**|[m_fltVal](../vs140/CDBVariant--m_fltVal.md)|  
|**DBVT_DOUBLE**|[m_dblVal](../vs140/CDBVariant--m_dblVal.md)|  
|**DBVT_DATE**|[m_pdate](../vs140/CDBVariant--m_pdate.md)|  
|**DBVT_STRING**|[m_pstring](../vs140/CDBVariant--m_pstring.md)|  
|**DBVT_BINARY**|[m_pbinary](../vs140/CDBVariant--m_pbinary.md)|  
|**DBVT_ASTRING**|[m_pstringA](../vs140/CDBVariant--m_pstringA.md)|  
|**DBVT_WSTRING**|[m_pstringW](../vs140/CDBVariant--m_pstringW.md)|  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDBVariant Class](../vs140/CDBVariant-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)