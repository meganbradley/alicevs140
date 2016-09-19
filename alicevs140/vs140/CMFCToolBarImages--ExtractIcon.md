---
title: "CMFCToolBarImages::ExtractIcon"
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
ms.assetid: c6a78963-416a-4296-b455-c35c8fae74b5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::ExtractIcon
Returns the icon that has a specified image index from the toolbar images.  
  
## Syntax  
  
```  
HICON ExtractIcon(  
   int nIndex   
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 The zero-based index in the image list at which the image to be extracted as an icon is located.  
  
## Return Value  
 A handle to the extracted icon, or `NULL` if `nIndex` is out of range.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)