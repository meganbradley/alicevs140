---
title: "CMFCColorMenuButton::IsEmptyMenuAllowed"
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
ms.assetid: 55e1535a-575b-446e-aedb-b0561f951f0b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorMenuButton::IsEmptyMenuAllowed
Indicates whether empty menus are supported.  
  
## Syntax  
  
```  
virtual BOOL IsEmptyMenuAllowed() const;  
```  
  
## Return Value  
 Nonzero if empty menus are allowed; otherwise, zero.  
  
## Remarks  
 Empty menus are supported by default. Override this method to change this behavior in derived class.  
  
## Requirements  
 **Header:** afxcolormenubutton.h  
  
## See Also  
 [CMFCColorMenuButton Class](../vs140/CMFCColorMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)