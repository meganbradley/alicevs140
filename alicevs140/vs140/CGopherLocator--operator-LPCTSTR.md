---
title: "CGopherLocator::operator LPCTSTR"
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
ms.assetid: 09830ab5-6a2b-4f10-a169-0e5aad5398c6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGopherLocator::operator LPCTSTR
This useful casting operator provides an efficient method to access the null-terminated C string contained in a `CGopherLocator` object.  
  
## Syntax  
  
```  
  
operator LPCTSTR ( ) const;  
  
```  
  
## Return Value  
 A character pointer to the string's data.  
  
## Remarks  
 No characters are copied; only a pointer is returned.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CGopherLocator Class](../vs140/CGopherLocator-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)