---
title: "CRecentFileList::operator"
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
ms.assetid: 7c8d5927-1c6d-4b7a-9ebc-6481782bbfd5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecentFileList::operator
The overloaded subscript (`[]`) operator returns a single `CString` specified by the zero-based index in `nIndex`.  
  
## Syntax  
  
```  
  
      CString& operator[ ](int nIndex);  
```  
  
#### Parameters  
 `nIndex`  
 Zero-based index of a `CString` in a set of `CString`s.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CRecentFileList Class](../vs140/CRecentFileList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)