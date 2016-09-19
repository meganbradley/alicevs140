---
title: "CMFCToolBarImages::IsValid"
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
ms.assetid: 1809311b-471d-4e4c-ad3b-930c378a4308
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::IsValid
Indicates whether this set of toolbar images contains a valid toolbar image.  
  
## Syntax  
  
```  
BOOL IsValid() const;  
```  
  
## Return Value  
 `TRUE` if a [CMFCToolbarImages](../vs140/CMFCToolBarImages-Class.md) object is valid; otherwise `FALSE`.  
  
## Remarks  
 The `CMFCToolBarImages` object is not valid when its handle to a bitmap with toolbar images is `NULL`.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)