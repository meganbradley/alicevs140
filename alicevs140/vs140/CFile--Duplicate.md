---
title: "CFile::Duplicate"
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
ms.assetid: aa4d7a62-284c-49f2-a2be-5cb0a4039a51
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::Duplicate
Constructs a duplicate `CFile` object for a given file.  
  
## Syntax  
  
```  
  
virtual CFile* Duplicate( ) const;  
```  
  
## Return Value  
 A pointer to a duplicate `CFile` object.  
  
## Remarks  
 This is equivalent to the C run-time function `_dup`.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)