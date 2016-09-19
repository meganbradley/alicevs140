---
title: "CMFCBaseTabCtrl::AddIcon"
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
ms.assetid: a3a2345d-9ff3-4fc2-9dc8-2602bea38d6e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::AddIcon
Adds an icon to the list of icons in the protected `CMap``m_mapAddedIcons` member.  
  
## Syntax  
  
```  
void AddIcon(  
   HICON hIcon,  
   int iIcon  
);  
```  
  
#### Parameters  
 [in] `hIcon`  
 A handle to the icon to be added.  
  
 [in] `iIcon`  
 Zero-based index of the icon in the protected `CImageList``m_Images` member.  
  
## Remarks  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)