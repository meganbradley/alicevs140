---
title: "CMFCToolBarImages::Save"
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
ms.assetid: 2a603999-37f8-4173-bc29-585fc7e4b10e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::Save
Stores the toolbar images in a file if this set of toolbar images contains user-defined images.  
  
## Syntax  
  
```  
BOOL Save(  
   LPCTSTR lpszBmpFileName=NULL   
);  
```  
  
#### Parameters  
 `lpszBmpFileName`  
 A path to a disk file.  
  
## Return Value  
 `TRUE` if the toolbar images were saved successfully; otherwise `FALSE`.  
  
## Remarks  
 Call this method to store the user-defined images into a disk file. If `lpszBmpFileName` is `NULL`, the method stores the bitmap into the file from which the bitmap was loaded by the [CMFCToolBarImages::Load](../vs140/CMFCToolBarImages--Load.md) method.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)