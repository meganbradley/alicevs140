---
title: "CDaoRecordset::m_pDatabase"
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
ms.assetid: 1531cec9-7dcf-4900-acad-edac310d22ae
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::m_pDatabase
Contains a pointer to the `CDaoDatabase` object through which the recordset is connected to a data source.  
  
## Remarks  
 This variable is set in two ways. Typically, you pass a pointer to an already open `CDaoDatabase` object when you construct the recordset object. If you pass **NULL** instead, **CDaoRecordset** creates a `CDaoDatabase` object for you and opens it. In either case, `CDaoRecordset` stores the pointer in this variable.  
  
 Normally you will not directly need to use the pointer stored in **m_pDatabase**. If you write your own extensions to `CDaoRecordset`, however, you might need to use the pointer. For example, you might need the pointer if you throw your own `CDaoException`(s).  
  
 For related information, see the topic "Database Object" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::m_pDAORecordset](../vs140/CDaoRecordset--m_pDAORecordset.md)