---
title: "CDBVariant::Clear"
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
ms.assetid: 05ca8d30-ce32-4858-a9b1-66685a22b00f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDBVariant::Clear
Call this member function to clear the `CDBVariant` object.  
  
## Syntax  
  
```  
  
void Clear( );  
  
```  
  
## Remarks  
 If the value of the [m_dwType](../vs140/CDBVariant--m_dwType.md) data member is **DBVT_DATE**, **DBVT_STRING**, or **DBVT_BINARY**, **Clear** frees the memory associated with the union pointer member. **Clear** sets `m_dwType` to **DBVT_NULL**.  
  
 The `CDBVariant` destructor calls **Clear**.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDBVariant Class](../vs140/CDBVariant-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDBVariant::m_dwType](../vs140/CDBVariant--m_dwType.md)