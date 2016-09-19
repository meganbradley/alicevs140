---
title: "CMFCToolBarImages::IsReadOnly"
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
ms.assetid: bdd42781-de0b-4030-b5d1-27e4a6455385
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::IsReadOnly
Specifies whether the toolbar images are read-only.  
  
## Syntax  
  
```  
BOOL IsReadOnly() const;  
```  
  
## Return Value  
 `TRUE` if the toolbar images are read-only, otherwise `FALSE`.  
  
## Remarks  
 The `CMFCToolbarImages` object is read-only when the bitmap with toolbar images was loaded from a read-only file, or when the bitmap was copied in using the `CMFCToolBarImages::CopyTemp`method.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)