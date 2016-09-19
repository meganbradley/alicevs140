---
title: "CAutoHideDockSite::m_nExtraSpace"
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
ms.assetid: dd4be432-7319-4716-ab52-0617f608d6ba
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoHideDockSite::m_nExtraSpace
The size of the space between the edges of the [CAutoHideDockSite Class](../vs140/CAutoHideDockSite-Class.md) and the [CMFCAutoHideBar Class](../vs140/CMFCAutoHideBar-Class.md) objects.  
  
## Syntax  
  
```  
static int m_nExtraSpace;  
```  
  
## Remarks  
 When a `CMFCAutoHideBar` is docked at a `CAutoHideDockSite`, it should not occupy the whole dock site. This global variable controls the extra space between the left or top border of the `CMFCAutoHideBar` and the corresponding `CAutoHideDockSite` edge. Whether the top or left edge is used depends on the current alignment.  
  
## Requirements  
 **Header:** afxautohidedocksite.h  
  
## See Also  
 [CAutoHideDockSite Class](../vs140/CAutoHideDockSite-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)