---
title: "CMFCToolBarImages::AddIcon"
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
ms.assetid: b4840649-c6a8-493c-9992-348918dfe696
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::AddIcon
Adds an icon to the list of toolbar images.  
  
## Syntax  
  
```  
int AddIcon(  
   HICON hIcon,  
   BOOL bAlphaBlend=FALSE   
);  
```  
  
#### Parameters  
 [in] `hIcon`  
 A handle to the icon to be added.  
  
 [in] `bAlphaBlend`  
 `TRUE` if this icon is used with alpha blending; otherwise `FALSE`.  
  
## Return Value  
 The zero-based index of the toolbar image that was added if the method is successful; otherwise -1.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)